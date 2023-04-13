# 202001221_Lab-7

# Name:Shah Harsh Sudarshan

# Section-A

Equivalence Partitioning Test Cases:

| Tester Action and Input Data               | Expected Outcome |
| :-------------:                            |:-------------:| 
| Valid input: day=1, month=1, year=1900     | Invalid date | 
| Valid input: day=31, month=12, year=2015   |  Previous date    |   
| Invalid input: day=0, month=6, year=2000   |  An error message | 
|Invalid input: day=32, month=6, year=2000	 |	An error message |
|Invalid input: day=29, month=2, year=2001	 |	An error message |

Boundary Value Analysis Test Cases:

| Tester Action and Input Data | Expected Outcome |
| :---------------------------------:|:----------------------:|
| Valid input: day=1, month=1, year=1900 | Invalid date |
| Valid input: day=31, month=12, year=2015 | Previous date |
| Invalid input: day=0, month=6, year=2000 | An error message |
| Invalid input: day=32, month=6, year=2000 | An error message |
| Invalid input: day=29, month=2, year=2000 | An error message |
| Valid input: day=1, month=6, year=2000 | Previous date |
| Valid input: day=31, month=5, year=2000 | Previous date |
| Valid input: day=15, month=6, year=2000 | Previous date |
| Invalid input: day=31, month=4, year=2000 | An error message |



**Problem1 :**

 ```java

  import static org.junit.Assert.*;

  import org.junit.Test;

  public class linearSearch {

    @Test
    public void test() 
    {
      LAB_7_P1 p1 = new LAB_7_P1();
      int v=2;
      int a[]=new int[] {4,3,2};
      assertEquals(2,p1.linearSearch(v,a));
    }


    @Test
    public void test2() 
    {
      LAB_7_P1 p1 = new LAB_7_P1();
      int v=3;
      int a[]=new int[] {4,2,1};
      assertEquals(-1,p1.linearSearch(v,a));
    }

    @Test
    public void test3() 
    {
      LAB_7_P1 p1 = new LAB_7_P1();
      int v=4;
      int a[]=new int[] {};
      assertEquals(-1,p1.linearSearch(v,a));
    }

    @Test
    public void test4() 
    {
      LAB_7_P1 p1 = new LAB_7_P1();
      int v=20;
      int a[]=new int[] {10,20,30,20,40};
      assertEquals(1,p1.linearSearch(v,a));
    }
  }

