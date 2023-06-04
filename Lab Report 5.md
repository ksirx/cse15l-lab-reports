__Name: Xavier Navarro__

__CSE 15L Lab Report 5__

In this lab report, I am doing to demonstrate the process of asking help for debugging. This is a process that we all have/had to go through before. Here is a demonstration of how this process should look like.

__Part 1: Debugging Scenario__

A student is having trouble with testing some code and decides to ask this on EdStem...

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

__What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?__

I am currently using a Windows computer (Dell XPS). I use the editor from VSCode with which I also use the terminal for bash.

__Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.__

Here is the output of the code when I run it:

[cs15lsp23cv@ieng6−202]:lab7:515 bash test.sh 

JUnit version 4.13.2 .E.E Time: 0.017 There were 2 failures:

testMerge1(ListExamplesTests) arrays first differed at element [0]; expected:<[a]> but was:<[x]> at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28) at org.junit.Assert.internalArrayEquals(Assert.java:534) at org.junit.Assert.assertArrayEquals(Assert.java:285) at org.junit.Assert.assertArrayEquals(Assert.java:300) at ListExamplesTests.testMerge1(ListExamplesTests.java:12) ... 9 trimmed Caused by: org.junit.ComparisonFailure: expected:<[a]> but was:<[x]> at org.junit.Assert.assertEquals(Assert.java:117) at org.junit.Assert.assertEquals(Assert.java:146) at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76) ... 15 more

testMerge2(ListExamplesTests) arrays first differed at element [0]; expected:<[a]> but was:<[c]> at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28) at org.junit.Assert.internalArrayEquals(Assert.java:534) at org.junit.Assert.assertArrayEquals(Assert.java:285) at org.junit.Assert.assertArrayEquals(Assert.java:300) at ListExamplesTests.testMerge2(ListExamplesTests.java:19) ... 9 trimmed Caused by: org.junit.ComparisonFailure: expected:<[a]> but was:<[c]> at org.junit.Assert.assertEquals(Assert.java:117) at org.junit.Assert.assertEquals(Assert.java:146) at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8) at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76) ... 15 more

FAILURES!!! Tests run: 2, Failures: 2

There seems to be issues with the code at the first element of the array. Both tests expected a in the first slot of the array, but instead it was x and c respectively that was found in index 0 of the array during the test.

__Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.__

Here is the code that was being run with the $ bash test.sh command that I used for the test.

```public class ListExamplesTests {
        @Test(timeout = 500)
        public void testMerge1() {
                List<String> l1 = new ArrayList<String>(Arrays.asList("x", "y"));
                List<String> l2 = new ArrayList<String>(Arrays.asList("a", "b"));
                assertArrayEquals(new String[]{ "a", "b", "x", "y"}, ListExamples.merge(l1, l2).toArray());
        }

        @Test(timeout = 500)
        public void testMerge2() {
                List<String> l1 = new ArrayList<String>(Arrays.asList("a", "b", "c"));
                List<String> l2 = new ArrayList<String>(Arrays.asList("c", "d", "e"));
                assertArrayEquals(new String[]{ "a", "b", "c", "c", "d", "e" }, ListExamples.merge(l1, l2).toArray());
        }

}
```

As you can see "a" is the expected value for both, but we are instead getting "x" for the first one, and "c" for the second one. Here's the code being run for the merge method...

```
static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list2.get(index2).compareTo(list1.get(index1)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      // change index1 below to index2 to fix test
      index2 += 1;
    }
    return result;
  }
  ```

Can you help me find what part of the code is causing the issue? I am really stuck and unsure of the changes that need to be made for the code to run as intended.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

