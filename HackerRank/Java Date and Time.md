# Java Date and Time

The Calendar class is an abstract class that provides methods for converting between a specific instant in time and a set of calendar fields such as YEAR, MONTH, DAY_OF_MONTH, HOUR, and so on, and for manipulating the calendar fields, such as getting the date of the next week.

The problem was to workout the DAY OF THE WEEK from a given DAY , MONTH and YEAR.

---

```JAVA
class Result {

    /*
     * Complete the 'findDay' function below.
     *
     * The function is expected to return a STRING.
     * The function accepts following parameters:
     *  1. INTEGER month JAN -> DEC 144025036146
     *  2. INTEGER day SAT -> FRI 0123456
     *  3. INTEGER year
     */

    public static String findDay(int month, int day, int year) {
        Calendar cal = Calendar.getInstance();
        cal.set(year, month-1, day);
        
        
        DateFormat formatter = new SimpleDateFormat("EEEE");
        String dayOfWeekString = formatter.format(cal.getTime()).toUpperCase();
        return dayOfWeekString;
    }

}
```
