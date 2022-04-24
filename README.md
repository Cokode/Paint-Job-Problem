# Paint-Job-Problem
Helping bob our friend calculate how many buckets of paints he needs to buy before going to work depending on the area he need to paint. 
public class PaintJob {

    public static void main(String[] args){
        System.out.println(getBucketCount(3.4, 2.1, 1.5, 2));
        System.out.println(getBucketCount(3.4, 2.1, 1.5));
        System.out.println(getBucketCount(3.26, 0.75));
    }

    public static int getBucketCount(double width, double height, double areaPerBucket, double extraBuckets){

        if(width <= 0 || height <= 0 || areaPerBucket <= 0 || extraBuckets < 0){
            return -1;
        }
        double area = width * height;
        double bukCount = area / areaPerBucket;
        double neededBuck = bukCount - extraBuckets;
        double result = Math.ceil(neededBuck);


        return (int) result;
    }

    public static int getBucketCount(double width, double height, double areaPerBucket){

        if(width <= 0 || height <= 0 || areaPerBucket <= 0 ){
            return -1;
        }
        double area = width * height;
        double bukCount = area / areaPerBucket;
        double neededBuck = Math.ceil(bukCount);

        return (int) neededBuck;
    }

    public static int getBucketCount(double area, double areaPerBucket){

        if(area <= 0 || areaPerBucket <= 0 ){
            return -1;
        }
        double bukCount = area / areaPerBucket;
        //System.out.println(bukCount);
        double neededBuck = Math.ceil(bukCount);

        return (int) neededBuck;
    }
}
