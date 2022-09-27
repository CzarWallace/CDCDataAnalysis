# CDCDataAnalysis
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.util.Collections;
import java.util.Scanner;
import java.util.Set;
import java.util.TreeSet;

import static java.util.Collections.*;

public class CDCDataAnalysis {


    public static void main(String args []) throws IOException {

        String stateName  ;
        int week = 0;
       // int dose = 0.0;


        BufferedReader br = new BufferedReader(new FileReader(".idea/COVID-19_Vaccine_Distribution_Allocations_by_Jurisdiction_-_Janssen.csv"));
        System.out.println("Row Labels      Average of 1st Dose Allocations");
        System.out.println("-------------------------------------------------");

        Set<CDCStates> cdcStatesSet = new TreeSet<>();
        Scanner inputStream = new Scanner(br);

     //   int [][] state = new int[(int) week][ dose];
       // for(int i = 0; i < file.length; i++)
        //String line = " ";

          while (inputStream.hasNextLine()){

              String line = inputStream.nextLine();
              String[]value = line.split(",");
              cdcStatesSet.add(new CDCStates(value[0], Integer.parseInt(value[1])));


             System.out.println("State: " + value[0] +"    " +  value[2]);
              break;
              //Text text1 = new Text("\nUnderline").setfont.setUnderline();
             // System.out.println("--------------------------------------");
              //break;

          }
        System.out.println();
    }


}





public class CDCStates implements Comparable<CDCStates>{

    private String jurisdiction;
    private int weekOfAllocations;
    private double dosePerWeek;

    public CDCStates(String jurisdiction, int weekOfAllocations) {
        this.jurisdiction = jurisdiction;
        this.weekOfAllocations = weekOfAllocations;
        this.dosePerWeek = dosePerWeek;
    }

    public String getJurisdiction() {
        return jurisdiction;
    }

    public int getWeekOfAllocations() {
        return weekOfAllocations;
    }

    public double getDosePerWeek() {
        return dosePerWeek;
    }

    @Override
    public String toString() {
        return "CDCStates{" +
                "jurisdiction='" + jurisdiction + '\'' +
                ", weekOfAllocations='" + weekOfAllocations  +
                ", dosePerWeek=" + dosePerWeek +
                '}';
    }

    @Override
    public int compareTo(CDCStates o) {
        return jurisdiction.compareTo(o.getJurisdiction());
    }


}


Jurisdiction,Week of Allocations,1st Dose Allocations
Connecticut,05/10/2021,6400
Maine,05/10/2021,2500
Massachusetts,05/10/2021,12300
New Hampshire,05/10/2021,2500
Rhode Island,05/10/2021,2000
Vermont,05/10/2021,1200
New Jersey,05/10/2021,15600
New York,05/10/2021,19800
New York City,05/10/2021,15100
Puerto Rico,05/10/2021,6100
U.S. Virgin Islands,05/10/2021,200
Delaware,05/10/2021,1700
District of Columbia,05/10/2021,1300
Maryland,05/10/2021,10500
Pennsylvania,05/10/2021,20000
Philadelphia,05/10/2021,2800
Virginia,05/10/2021,14800
West Virginia,05/10/2021,3300
Alabama,05/10/2021,8500
Florida,05/10/2021,37000
Georgia,05/10/2021,17600
Kentucky,05/10/2021,7800
Mississippi,05/10/2021,5100
North Carolina,05/10/2021,17700
South Carolina,05/10/2021,8700
Tennessee,05/10/2021,11600
Chicago,05/10/2021,4800
Illinois,05/10/2021,17600
Indiana,05/10/2021,11400
Michigan,05/10/2021,17500
Minnesota,05/10/2021,9600
Ohio,05/10/2021,20300
Wisconsin,05/10/2021,10200
Arkansas,05/10/2021,5200
Louisiana,05/10/2021,8000
New Mexico,05/10/2021,3600
Oklahoma,05/10/2021,6700
Texas,05/10/2021,46300
Iowa,05/10/2021,5500
Kansas,05/10/2021,5000
Missouri,05/10/2021,10600
Nebraska,05/10/2021,3300
Colorado,05/10/2021,9700
Montana,05/10/2021,1900
North Dakota,05/10/2021,1400
South Dakota,05/10/2021,1500
Utah,05/10/2021,4900
Wyoming,05/10/2021,1000
Arizona,05/10/2021,12000
California,05/10/2021,67600
Hawaii,05/10/2021,2600
Nevada,05/10/2021,5100
American Samoa,05/10/2021,0
Guam,05/10/2021,0
Marshall Islands,05/10/2021,0
Micronesia,05/10/2021,0
Mariana Islands,05/10/2021,0
Palau,05/10/2021,0
Alaska,05/10/2021,1900
Idaho,05/10/2021,2900
Oregon,05/10/2021,7300
Washington,05/10/2021,12900
Federal Entities,05/10/2021,33200
Connecticut,05/03/2021,8300
Maine,05/03/2021,3200
Massachusetts,05/03/2021,16000
New Hampshire,05/03/2021,3200
Rhode Island,05/03/2021,2500
Vermont,05/03/2021,1500
New Jersey,05/03/2021,20200
New York,05/03/2021,25700
New York City,05/03/2021,19500
Puerto Rico,05/03/2021,7900
U.S. Virgin Islands,05/03/2021,300
Delaware,05/03/2021,2200
District of Columbia,05/03/2021,1700
Maryland,05/03/2021,13600
Pennsylvania,05/03/2021,26000
Philadelphia,05/03/2021,3600
Virginia,05/03/2021,19200
West Virginia,05/03/2021,4300
Alabama,05/03/2021,11000
Florida,05/03/2021,48100
Georgia,05/03/2021,22800
Kentucky,05/03/2021,10100
Mississippi,05/03/2021,6700
North Carolina,05/03/2021,23000
South Carolina,05/03/2021,11300
Tennessee,05/03/2021,15100
Chicago,05/03/2021,6200
Illinois,05/03/2021,22800
Indiana,05/03/2021,14800
Michigan,05/03/2021,22700
Minnesota,05/03/2021,12400
Ohio,05/03/2021,26400
Wisconsin,05/03/2021,13200
Arkansas,05/03/2021,6700
Louisiana,05/03/2021,10400
New Mexico,05/03/2021,4800
Oklahoma,05/03/2021,8700
Texas,05/03/2021,60100
Iowa,05/03/2021,7100
Kansas,05/03/2021,6400
Missouri,05/03/2021,13800
Nebraska,05/03/2021,4300
Colorado,05/03/2021,12500
Montana,05/03/2021,2400
North Dakota,05/03/2021,1800
South Dakota,05/03/2021,2000
Utah,05/03/2021,6300
Wyoming,05/03/2021,1300
Arizona,05/03/2021,15600
California,05/03/2021,87800
Hawaii,05/03/2021,3300
Nevada,05/03/2021,6600
American Samoa,05/03/2021,0
Guam,05/03/2021,0
Marshall Islands,05/03/2021,0
Micronesia,05/03/2021,0
Mariana Islands,05/03/2021,0
Palau,05/03/2021,0
Alaska,05/03/2021,2500
Idaho,05/03/2021,3700
Oregon,05/03/2021,9500
Washington,05/03/2021,16700
Federal Entities,05/03/2021,25700
Connecticut,04/12/2021,6400
Maine,04/12/2021,2500
Massachusetts,04/12/2021,12300
New Hampshire,04/12/2021,2500
Rhode Island,04/12/2021,2000
Vermont,04/12/2021,1200
New Jersey,04/12/2021,15600
New York,04/12/2021,19800
New York City,04/12/2021,15100
Puerto Rico,04/12/2021,6100
U.S. Virgin Islands,04/12/2021,200
Delaware,04/12/2021,1700
District of Columbia,04/12/2021,1300
Maryland,04/12/2021,10500
Pennsylvania,04/12/2021,20000
Philadelphia,04/12/2021,2800
Virginia,04/12/2021,14800
West Virginia,04/12/2021,3300
Alabama,04/12/2021,8500
Florida,04/12/2021,37000
Georgia,04/12/2021,17600
Kentucky,04/12/2021,7800
Mississippi,04/12/2021,5100
North Carolina,04/12/2021,17700
South Carolina,04/12/2021,8700
Tennessee,04/12/2021,11600
Chicago,04/12/2021,4800
Illinois,04/12/2021,17600
Indiana,04/12/2021,11400
Michigan,04/12/2021,17500
Minnesota,04/12/2021,9600
Ohio,04/12/2021,20300
Wisconsin,04/12/2021,10200
Arkansas,04/12/2021,5200
Louisiana,04/12/2021,8000
New Mexico,04/12/2021,3700
Oklahoma,04/12/2021,6700
Texas,04/12/2021,46300
Iowa,04/12/2021,5400
Kansas,04/12/2021,5000
Missouri,04/12/2021,10600
Nebraska,04/12/2021,3300
Colorado,04/12/2021,9700
Montana,04/12/2021,1900
North Dakota,04/12/2021,1400
South Dakota,04/12/2021,1500
Utah,04/12/2021,4900
Wyoming,04/12/2021,1000
Arizona,04/12/2021,12000
California,04/12/2021,67600
Hawaii,04/12/2021,2600
Nevada,04/12/2021,5100
American Samoa,04/12/2021,0
Guam,04/12/2021,0
Marshall Islands,04/12/2021,0
Micronesia,04/12/2021,0
Mariana Islands,04/12/2021,0
Palau,04/12/2021,0
Alaska,04/12/2021,1900
Idaho,04/12/2021,2900
Oregon,04/12/2021,7300
Washington,04/12/2021,12900
Federal Entities,04/12/2021,129600
Connecticut,04/05/2021,53900
Maine,04/05/2021,20600
Massachusetts,04/05/2021,103800
New Hampshire,04/05/2021,20600
Rhode Island,04/05/2021,16200
Vermont,04/05/2021,9700
New Jersey,04/05/2021,131600
New York,04/05/2021,167600
New York City,04/05/2021,127200
Puerto Rico,04/05/2021,51400
U.S. Virgin Islands,04/05/2021,1600
Delaware,04/05/2021,14300
District of Columbia,04/05/2021,10800
Maryland,04/05/2021,88800
Pennsylvania,04/05/2021,169200
Philadelphia,04/05/2021,23500
Virginia,04/05/2021,124700
West Virginia,04/05/2021,27800
Alabama,04/05/2021,71800
Florida,04/05/2021,313200
Georgia,04/05/2021,148500
Kentucky,04/05/2021,65300
Mississippi,04/05/2021,43200
North Carolina,04/05/2021,149800
South Carolina,04/05/2021,73500
Tennessee,04/05/2021,98100
Chicago,04/05/2021,39900
Illinois,04/05/2021,148600
Indiana,04/05/2021,96500
Michigan,04/05/2021,147800
Minnesota,04/05/2021,80800
Ohio,04/05/2021,171900
Wisconsin,04/05/2021,85900
Arkansas,04/05/2021,43500
Louisiana,04/05/2021,67700
New Mexico,04/05/2021,30800
Oklahoma,04/05/2021,56400
Texas,04/05/2021,392100
Iowa,04/05/2021,45800
Kansas,04/05/2021,41800
Missouri,04/05/2021,89600
Nebraska,04/05/2021,27600
Colorado,04/05/2021,81400
Montana,04/05/2021,15600
North Dakota,04/05/2021,11300
South Dakota,04/05/2021,12500
Utah,04/05/2021,40700
Wyoming,04/05/2021,8500
Arizona,04/05/2021,101700
California,04/05/2021,572700
Hawaii,04/05/2021,21300
Nevada,04/05/2021,42900
American Samoa,04/05/2021,3700
Guam,04/05/2021,16900
Marshall Islands,04/05/2021,9600
Micronesia,04/05/2021,15900
Mariana Islands,04/05/2021,1600
Palau,04/05/2021,3200
Alaska,04/05/2021,15800
Idaho,04/05/2021,23800
Oregon,04/05/2021,61400
Washington,04/05/2021,109000
Federal Entities,04/05/2021,84600
Connecticut,03/29/2021,21200
Maine,03/29/2021,8100
Massachusetts,03/29/2021,40800
New Hampshire,03/29/2021,8100
Rhode Island,03/29/2021,6400
Vermont,03/29/2021,3900
New Jersey,03/29/2021,51700
New York,03/29/2021,65800
New York City,03/29/2021,49900
Puerto Rico,03/29/2021,20300
U.S. Virgin Islands,03/29/2021,700
Delaware,03/29/2021,5600
District of Columbia,03/29/2021,4300
Maryland,03/29/2021,34900
Pennsylvania,03/29/2021,66400
Philadelphia,03/29/2021,9200
Virginia,03/29/2021,49000
West Virginia,03/29/2021,11000
Alabama,03/29/2021,28300
Florida,03/29/2021,122900
Georgia,03/29/2021,58400
Kentucky,03/29/2021,25700
Mississippi,03/29/2021,17100
North Carolina,03/29/2021,58800
South Carolina,03/29/2021,28900
Tennessee,03/29/2021,38600
Chicago,03/29/2021,15700
Illinois,03/29/2021,58400
Indiana,03/29/2021,38000
Michigan,03/29/2021,58100
Minnesota,03/29/2021,31800
Ohio,03/29/2021,67400
Wisconsin,03/29/2021,33800
Arkansas,03/29/2021,17200
Louisiana,03/29/2021,26600
New Mexico,03/29/2021,12100
Oklahoma,03/29/2021,22200
Texas,03/29/2021,153900
Iowa,03/29/2021,18100
Kansas,03/29/2021,16500
Missouri,03/29/2021,35200
Nebraska,03/29/2021,10900
Colorado,03/29/2021,32000
Montana,03/29/2021,6100
North Dakota,03/29/2021,4500
South Dakota,03/29/2021,5000
Utah,03/29/2021,16100
Wyoming,03/29/2021,3400
Arizona,03/29/2021,40000
California,03/29/2021,224600
Hawaii,03/29/2021,8400
Nevada,03/29/2021,16900
American Samoa,03/29/2021,300
Guam,03/29/2021,900
Marshall Islands,03/29/2021,400
Micronesia,03/29/2021,600
Mariana Islands,03/29/2021,400
Palau,03/29/2021,200
Alaska,03/29/2021,6300
Idaho,03/29/2021,9500
Oregon,03/29/2021,24200
Washington,03/29/2021,42800
Federal Entities,03/29/2021,16700
Connecticut,03/22/2021,4200
Maine,03/22/2021,1600
Massachusetts,03/22/2021,8000
New Hampshire,03/22/2021,1600
Rhode Island,03/22/2021,1300
Vermont,03/22/2021,800
New Jersey,03/22/2021,10200
New York,03/22/2021,12900
New York City,03/22/2021,9800
Puerto Rico,03/22/2021,4000
U.S. Virgin Islands,03/22/2021,200
Delaware,03/22/2021,1100
District of Columbia,03/22/2021,900
Maryland,03/22/2021,6900
Pennsylvania,03/22/2021,13000
Philadelphia,03/22/2021,1800
Virginia,03/22/2021,9600
West Virginia,03/22/2021,2200
Alabama,03/22/2021,5600
Florida,03/22/2021,24100
Georgia,03/22/2021,11500
Kentucky,03/22/2021,5100
Mississippi,03/22/2021,3400
North Carolina,03/22/2021,11500
South Carolina,03/22/2021,5700
Tennessee,03/22/2021,7600
Chicago,03/22/2021,3100
Illinois,03/22/2021,11500
Indiana,03/22/2021,7500
Michigan,03/22/2021,11400
Minnesota,03/22/2021,6300
Ohio,03/22/2021,13200
Wisconsin,03/22/2021,6700
Arkansas,03/22/2021,3400
Louisiana,03/22/2021,5200
New Mexico,03/22/2021,2400
Oklahoma,03/22/2021,4400
Texas,03/22/2021,30200
Iowa,03/22/2021,3600
Kansas,03/22/2021,3300
Missouri,03/22/2021,6900
Nebraska,03/22/2021,2200
Colorado,03/22/2021,6300
Montana,03/22/2021,1200
North Dakota,03/22/2021,900
South Dakota,03/22/2021,1000
Utah,03/22/2021,3200
Wyoming,03/22/2021,700
Arizona,03/22/2021,7900
California,03/22/2021,44000
Hawaii,03/22/2021,1700
Nevada,03/22/2021,3300
American Samoa,03/22/2021,100
Guam,03/22/2021,200
Marshall Islands,03/22/2021,100
Micronesia,03/22/2021,100
Mariana Islands,03/22/2021,100
Palau,03/22/2021,100
Alaska,03/22/2021,1300
Idaho,03/22/2021,1900
Oregon,03/22/2021,4800
Washington,03/22/2021,8400
Federal Entities,03/22/2021,16700
Connecticut,03/15/2021,4200
Maine,03/15/2021,1600
Massachusetts,03/15/2021,8000
New Hampshire,03/15/2021,1600
Rhode Island,03/15/2021,1300
Vermont,03/15/2021,800
New Jersey,03/15/2021,10200
New York,03/15/2021,12900
New York City,03/15/2021,9800
Puerto Rico,03/15/2021,4000
U.S. Virgin Islands,03/15/2021,200
Delaware,03/15/2021,1100
District of Columbia,03/15/2021,900
Maryland,03/15/2021,6900
Pennsylvania,03/15/2021,13000
Philadelphia,03/15/2021,1800
Virginia,03/15/2021,9600
West Virginia,03/15/2021,2200
Alabama,03/15/2021,5600
Florida,03/15/2021,24100
Georgia,03/15/2021,11500
Kentucky,03/15/2021,5100
Mississippi,03/15/2021,3400
North Carolina,03/15/2021,11500
South Carolina,03/15/2021,5700
Tennessee,03/15/2021,7600
Chicago,03/15/2021,3100
Illinois,03/15/2021,11500
Indiana,03/15/2021,7500
Michigan,03/15/2021,11400
Minnesota,03/15/2021,6300
Ohio,03/15/2021,13200
Wisconsin,03/15/2021,6700
Arkansas,03/15/2021,3400
Louisiana,03/15/2021,5200
New Mexico,03/15/2021,2400
Oklahoma,03/15/2021,4400
Texas,03/15/2021,30200
Iowa,03/15/2021,3600
Kansas,03/15/2021,3300
Missouri,03/15/2021,6900
Nebraska,03/15/2021,2200
Colorado,03/15/2021,6300
Montana,03/15/2021,1200
North Dakota,03/15/2021,900
South Dakota,03/15/2021,1000
Utah,03/15/2021,3200
Wyoming,03/15/2021,700
Arizona,03/15/2021,7900
California,03/15/2021,44000
Hawaii,03/15/2021,1700
Nevada,03/15/2021,3300
American Samoa,03/15/2021,100
Guam,03/15/2021,200
Marshall Islands,03/15/2021,100
Micronesia,03/15/2021,100
Mariana Islands,03/15/2021,100
Palau,03/15/2021,100
Alaska,03/15/2021,1300
Idaho,03/15/2021,1900
Oregon,03/15/2021,4800
Washington,03/15/2021,8400
Federal Entities,03/15/2021,120500
Connecticut,03/01/2021,30200
Maine,03/01/2021,11500
Massachusetts,03/01/2021,58100
New Hampshire,03/01/2021,11600
Rhode Island,03/01/2021,9100
Vermont,03/01/2021,5400
New Jersey,03/01/2021,73600
New York,03/01/2021,93700
New York City,03/01/2021,71100
Puerto Rico,03/01/2021,28800
U.S. Virgin Islands,03/01/2021,900
Delaware,03/01/2021,8000
District of Columbia,03/01/2021,6000
Maryland,03/01/2021,49600
Pennsylvania,03/01/2021,94600
Philadelphia,03/01/2021,13100
Virginia,03/01/2021,69700
West Virginia,03/01/2021,15500
Alabama,03/01/2021,40100
Florida,03/01/2021,175100
Georgia,03/01/2021,83000
Kentucky,03/01/2021,36500
Mississippi,03/01/2021,24200
North Carolina,03/01/2021,83700
South Carolina,03/01/2021,41100
Tennessee,03/01/2021,54800
Chicago,03/01/2021,22300
Illinois,03/01/2021,83100
Indiana,03/01/2021,53900
Michigan,03/01/2021,82700
Minnesota,03/01/2021,45200
Ohio,03/01/2021,96100
Wisconsin,03/01/2021,48000
Arkansas,03/01/2021,24400
Louisiana,03/01/2021,37900
New Mexico,03/01/2021,17200
Oklahoma,03/01/2021,31500
Texas,03/01/2021,219200
Iowa,03/01/2021,25600
Kansas,03/01/2021,23400
Missouri,03/01/2021,50100
Nebraska,03/01/2021,15500
Colorado,03/01/2021,45500
Montana,03/01/2021,8700
North Dakota,03/01/2021,6300
South Dakota,03/01/2021,7000
Utah,03/01/2021,22800
Wyoming,03/01/2021,4800
Arizona,03/01/2021,56800
California,03/01/2021,320100
Hawaii,03/01/2021,11900
Nevada,03/01/2021,24000
American Samoa,03/01/2021,400
Guam,03/01/2021,1300
Marshall Islands,03/01/2021,600
Micronesia,03/01/2021,800
Mariana Islands,03/01/2021,400
Palau,03/01/2021,200
Alaska,03/01/2021,8900
Idaho,03/01/2021,13300
Oregon,03/01/2021,34400
Washington,03/01/2021,60900
Federal Entities,03/01/2021,139200

