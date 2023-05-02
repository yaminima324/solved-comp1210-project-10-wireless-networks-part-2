Download Link: https://assignmentchef.com/product/solved-comp1210-project-10-wireless-networks-part-2
<br>
Files to submit to Web-CAT:

<u>From Project 9</u>

<ul>

 <li>java</li>

 <li>java, WiFiTest.java</li>

 <li>java, CellularTest.java</li>

 <li>java, LTETest.java</li>

 <li>java, FiveGTest.java</li>

</ul>

<u>New in Project 10</u>

<ul>

 <li>java, BandwidthComparatorTest.java</li>

 <li>java, MonthlyCostComparatorTest.java</li>

 <li>java, WirelessNetworkListTest.java</li>

 <li>java, WirelessNetworksPart2Test.java</li>

</ul>

<h1>Recommendations</h1>

You should create new folder for Project 10 and copy your relevant Project 9 source and test files to it. You should create a jGRASP project and add the new source and test files as they are created<strong> </strong>

<strong>Specifications – </strong><strong>Use arrays in this project; ArrayLists are not allowed! </strong>

<strong>Overview</strong>:  This project is the second of three that will involve the monthly cost and reporting for wireless networks.  In Part 1 you developed Java classes that represent categories of wireless networks including WiFi, cellular, LTE, and 5G. In Part 2, you will implement four additional classes: (1) BandwidthComparator that implements the Comparator interface for WirelessNetwork, (2) MonthlyCostComparator that implements the Comparator interface for WirelessNetwork, (3) WirelessNetworkList that represents a list of wireless networks and includes several specialized methods, and (4) WirelessNetworksPart2 which contains the main method for the program.   Note that the main method in WirelessNetworksPart2 should create a WirelessNetworkList object and then call the readFile method on the WirelessNetworkList object, which will add wireless networks to the list as the data is read in from a file.  You can use WirelessNetworksPart2 in conjunction with interactions by running the program in a jGRASP canvas (or debugger with a breakpoint) and single stepping until the variables of interest are created.  You can then enter interactions in the usual way. In addition to the source files, you will create a JUnit test file for each class and write one or more test methods to ensure the classes and methods meet the specifications.  <u>You should create a jGRASP</u> <u>project upfront and then add the new source and test files as they are created.  All of your files should</u> <u>be in a single folder</u>.




<ul>

 <li><strong>WiFi, Cellular, LTE, and FiveG </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design</strong>: No changes from the specifications in Part 1.




<ul>

 <li><strong>java </strong></li>

</ul>

<strong>                </strong>

<strong>Requirements and Design</strong>: <u>In addition to the specifications in Part 1</u>, the WirelessNetwork class should implement the Comparable interface for WirelessNetwork, which means the following method must be implemented in WirelessNetwork.

o compareTo:  Takes a WirelessNetwork as a parameter and returns an int indicating the results of comparing the two WirelessNetwork object based on their respective name fields.




<ul>

 <li><strong>java </strong></li>

</ul>




<strong>Requirements: </strong>The WirelessNetworkList class provides methods for reading in the data file and generating reports.

<strong> </strong>

<strong>Design: </strong>The WirelessNetworkList class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields:</strong> 1) An array of WirelessNetwork objects and 2) an array of String elements to hold invalid records read from the data file. [The second array will be used in Part 3.] Note that there are no fields for the number elements in each array.  In this project, <u>the size of the array</u> <u>should be the same as the number of elements in the array</u>. These two fields should be private.</li>

 <li><strong>Constructor: </strong>The constructor has no parameters and initializes the WirelessNetwork array and String array in the fields to arrays of length 0.</li>

 <li><strong>Methods:</strong> Usually a class provides methods to access and modify each of its instance variables (i.e., getters and setters) along with any other required methods. The methods for WirelessNetworkList are described below.

  <ul>

   <li>getWirelessNetworksArray returns an array of type WirelessNetwork representing the WirelessNetwork array field.</li>

   <li>getInvalidRecordsArray returns an array of type String representing the invalid records array field.</li>

   <li>addWirelessNetwork has no return value, accepts a WirelessNetwork object, increases the capacity of the WirelessNetwork array by one, and adds the WirelessNetwork in the last position of the WirelessNetwork array.</li>

   <li>addInvalidRecord has no return value, accepts a String, increases the capacity of the invalidRecords array by one, and adds the String in the last position of the invalidRecords array. This method will be used in Project 11, but it still needs to be tested in this project.</li>

   <li>readFile has no return value, accepts the data file name as a String, and throws FileNotFoundException. This method creates a Scanner object to read in the file one line at a time.  When a line is read, a separate Scanner object on the line should be created to</li>

  </ul></li>

</ul>

read the values in that line.  The data in each line is separated by a semicolon so the delimiter should be set to comma by invoking the useDelimiter(“,”) method on the Scanner object for the line. For each line read in, the appropriate WirelessNetwork object is created and added to the WirelessNetwork array field, or if not a valid category code, the line should be ignored.  The data file has comma-delimited text records as follows: category, name, bandwidth, fixed monthly cost, followed by one or more fields specific to the category.  Remember, WiFi, Cellular, LTE, and FiveG objects are all WirelessNetwork objects.  The category codes are W for WiFi, C for Cellular, L for LTE, and F for FiveG.  Any other category code is invalid.  Below are examples data records:

W,My Wifi,450,40.00,5.00

C,My Note,5.0,20.00,1200,1.0

X,Bad Data,0,0,0,0,0,0,0

L,My iPad,20.0,30.00,1200,2.0

F,My Phone,80.0,50.00,1200,10.0

<ul>

 <li>generateReport processes the WirelessNetwork array using the <u>original order</u> from the file to produce the Monthly Wireless Network Report and then returns the report as String. See example result in output for WirelessNetworksPart2 beginning on page 6. o generateReportByName sorts the WirelessNetwork array by its <u>natural ordering</u>, and processes the WirelessNetwork array to produce the Monthly Wireless Network Report (by Name), then returns the report as a String.  See example result in output for WirelessNetworksPart2 beginning on page 6.</li>

 <li>generateReportByBandwidth sorts the WirelessNetwork array by its <u>bandwidth</u>, and processes the WirelessNetwork array to produce the Monthly Wireless Network Report (by Bandwidth), then returns the report as a String. See example result in output for WirelessNetworksPart2 beginning on page 6.</li>

 <li>generateReportByMonthtlyCost sorts the WirelessNetwork array <u>by monthly</u> <u>cost</u>, and processes the WirelessNetwork array to produce the Monthly Wireless Network Report (by Monthly Cost) and then returns the report as String. See example result in output for WirelessNetworksPart2 beginning on page 6.</li>

</ul>




<strong>Code and Test:</strong>  See examples of file reading and sorting (using Arrays.sort) in the class notes.




The natural sorting order based on a wireless network’s name for is determined by the compareTo method when the Comparable interface is implemented.

Arrays.sort(getWirelessNetworksArray());




The sorting order based on a wireless network’s bandwidth is determined by the

BandwidthComparator class which implements the Comparator interface (described below).<strong>                           </strong>

Arrays.sort(getWirelessNetworksArray(), new BandwidthComparator());

The sorting order based on a wireless network’s monthly cost is determined by the

MonthlyCostComparator class which implements the Comparator interface (described below).<strong>    </strong>

Arrays.sort(getWirelessNetworksArray(), new MonthlyCostComparator());




In your JUnit test methods for the generate reports methods above, you may want to use the following assertion to avoid having to match the return result exactly (where the expected_result is part of what you think it should contain and the actual_result is the result of the method call.

Assert.assertTrue(actual_result.contains(expected_result));

<ul>

 <li><strong>BandwidthComparator</strong><strong>.java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design: </strong>The BandwidthComparator class implements the Comparator interface for WirelessNetwork objects.  Hence, it implements the method

compare(WirelessNetwork n1, WirelessNetwork n2) that defines the ordering from <u>lowest to highest</u> based on the wireless network’s bandwidth.  See examples in class notes.

<strong> </strong>

<ul>

 <li><strong>MonthlyCostComparator</strong><strong>.java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design: </strong>The MonthlyCostComparator class implements the Comparator interface for WirelessNetwork objects.  Hence, it implements the method

compare(WirelessNetwork n1, WirelessNetwork n2) that defines the ordering from <u>highest to lowest</u> based on the wireless network’s monthly cost.  See examples in class notes.

<strong> </strong>

<ul>

 <li><strong>java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements: </strong>The WirelessNetworksPart2 class contains the main method for running the program.




<strong>Design: </strong>The WirelessNetworksPart2 class is the driver class and has a main method described below.




o main accepts a file name as a command line argument, creates a WirelessNetworkList object, and then invokes its methods to read the file and process the wireless network records and then to generate and print the four reports as shown in the example output beginning on page 6.  If no command line argument is provided, the program should indicate this and end as shown in the first example output on page 5.  An example data file can be downloaded from the assignment page in Canvas.




<strong>Code and Test:  </strong>In your JUnit test file for the WirelessNetworksPart2 class, you should have at least two test methods for the main method.  One test method should invoke

WirelessNetworksPart2.main(args) where args is an empty String array, and the other test method should invoke WirelessNetworksPart2.main(args) where args[0] is the String representing the data file name. Depending on how you implemented the main method, these two methods should cover the code in main.  As for the assertion in the test method, since COST_FACTOR is a public class variable in Cellular, you could assert that Cellular.COST_FACTOR equals 1.0 in each test methods.

<strong> </strong>

In the first test method, you can invoke main with no command line argument as follows:

// If you are checking for args.length == 0

// in WirelessNetworksPart2, the following should exercise

// the code for true.

String[] args1 = {};  // an empty String[]

WirelessNetworksPart2.main(args1);




In the second test method, you can invoke main as follows with the file name as the first (and only) command line argument:

String[] args2 = {” wireless_network_data1.csv”};

// args2[0] is the file name

WirelessNetworksPart2.main(args2);




If Web-CAT complains the default constructor for WirelessNetworksPart2 has not been covered, you should include the following line of code in one of your test methods.

// to exercise the default constructor

WirelessNetworksPart2 app = new WirelessNetworksPart2();




<strong>Notes: </strong>

<ol>

 <li>Passing in command line arguments in jGRASP – On the top menu, click “Build” then turn on “Run Arguments” by clicking the associated checkbox. Now you can enter the arguments (e.g., the filename) in the Run Arguments text box at the top of the edit window containing the main method. Finally, run or debug the program in the usual way.</li>

</ol>




<ol start="2">

 <li>To run the program with no command line argument, either delete the text entered above.</li>

</ol>

Alternatively, click “Build” then turn off “Run Arguments” by clicking the associated checkbox. Then run or debug the program in the usual way.




<ol start="3">

 <li>You can also test your program using your own data files.</li>

</ol>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>Example Output when file name is missing as command line argument</h1>

<strong> </strong>

MM«M —-jGRASP exec: java WirelessNetworksPart2 MM§MFile name expected as command line argument. MM§MProgram ending. MM§M

MM©M —-jGRASP: operation complete.

<strong> </strong>




<strong> </strong>

<strong> </strong>

<table>

 <tbody>

  <tr>

   <td width="90"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<h2>Example Output for wireless_network_data1.csv</h2>

<strong> </strong>

<table width="639">

 <tbody>

  <tr>

   <td width="639">MM«M —-jGRASP exec: java WirelessNetworksPart2 wireless_network_data1.csvMM§M——————————-MM§MMonthly Wireless Network ReportMM§M——————————-MM§MMy Wifi (class WiFi) Cost: $45.00MM§MBandwidth: 450.0 MbpsMM§MMM§MMy Note (class Cellular) Cost: $20.00MM§MBandwidth: 5.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 1.0 GBMM§MData Used: 0.75 GBMM§MMM§MMy iPad (class LTE) Cost: $38.00MM§MBandwidth: 20.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 2.0 GB MM§MData Used: 3.0 GBMM§MMM§MMy Phone (class FiveG) Cost: $80.00MM§MBandwidth: 80.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 10.0 GB MM§MData Used: 12.0 GBMM§MMM§M—————————————–MM§MMonthly Wireless Network Report (by Name)MM§M—————————————–MM§MMy iPad (class LTE) Cost: $38.00MM§MBandwidth: 20.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 2.0 GB MM§MData Used: 3.0 GBMM§MMM§MMy Note (class Cellular) Cost: $20.00MM§MBandwidth: 5.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 1.0 GBMM§MData Used: 0.75 GBMM§MMM§MMy Phone (class FiveG) Cost: $80.00MM§MBandwidth: 80.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 10.0 GB MM§MData Used: 12.0 GBMM§MMM§MMy Wifi (class WiFi) Cost: $45.00MM§MBandwidth: 450.0 MbpsMM§M</td>

  </tr>

  <tr>

   <td width="639">MM§M———————————————-MM§MMonthly Wireless Network Report (by Bandwidth)MM§M———————————————-MM§MMy Note (class Cellular) Cost: $20.00MM§MBandwidth: 5.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 1.0 GBMM§MData Used: 0.75 GBMM§MMM§MMy iPad (class LTE) Cost: $38.00MM§MBandwidth: 20.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 2.0 GB MM§MData Used: 3.0 GBMM§MMM§MMy Phone (class FiveG) Cost: $80.00MM§MBandwidth: 80.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 10.0 GB MM§MData Used: 12.0 GBMM§MMM§MMy Wifi (class WiFi) Cost: $45.00MM§MBandwidth: 450.0 MbpsMM§MMM§M————————————————-MM§MMonthly Wireless Network Report (by Monthly Cost)MM§M————————————————-MM§MMy Phone (class FiveG) Cost: $80.00MM§MBandwidth: 80.0 MbpsMM§MTime: 1200.0 secondsMM§MData Limit: 10.0 GB MM§MData Used: 12.0 GBMM§MMM§MMy Wifi (class WiFi) Cost: $45.00MM§MBandwidth: 450.0 MbpsMM§MMM§MMy iPad (class LTE) Cost: $38.00MM§MBandwidth: 20.0 MbpsMM§MTime: 1200.0 seconds MM§MData Limit: 2.0 GB MM§MData Used: 3.0 GBMM§MMM§MMy Note (class Cellular) Cost: $20.00MM§MBandwidth: 5.0 MbpsMM§MTime: 1200.0 seconds MM§MData Limit: 1.0 GBMM§MData Used: 0.75 GBMM§MMM§MMM©M —-jGRASP: operation complete.<strong> </strong></td>

  </tr>

 </tbody>

</table>