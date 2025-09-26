# Inheritance
Here is the link to my flowchart:
https://app.diagrams.net/#G1M3QDy2ZXQznKbDJvML84HprWI_E6xTTd#%7B%22pageId%22%3A%22La6DI70zyOqZkMgaT3Lr%22%7D
Here is the link to the code:
https://onecompiler.com/java/43xtwg6tw
Here is the link to my video:
https://screenpal.com/content/video/cTQOfHnD0Nh?top-banner=online-recorder-details
Here is the actual code:
public class Main {
    public static void main(String[] args) {
        // Create the Course object with provided data
        Course course1 = new Course();
        course1.setCourseNumber("ECE287");
        course1.setCourseTitle("Digital Systems Design");

        // Create the OfferedCourse object with provided data
        OfferedCourse course2 = new OfferedCourse();
        course2.setCourseNumber("ECE387");
        course2.setCourseTitle("Embedded Systems Design");
        course2.setInstructorName("Mark Patterson");
        course2.setLocation("Wilson Hall 231");
        course2.setClassTime("WF: 2-3:30 pm");

        // Print expected outputs
        course1.printInfo();
        course2.printInfo();
    }
}

// Base class: Course
class Course {
    private String courseNumber;
    private String courseTitle;

    public void setCourseNumber(String number) {
        this.courseNumber = number;
    }

    public String getCourseNumber() {
        return this.courseNumber;
    }

    public void setCourseTitle(String title) {
        this.courseTitle = title;
    }

    public String getCourseTitle() {
        return this.courseTitle;
    }

    public void printInfo() {
        System.out.println("Course Information:");
        System.out.println("   Course Number: " + getCourseNumber());
        System.out.println("   Course Title: " + getCourseTitle());
    }
}

// Derived class: OfferedCourse
class OfferedCourse extends Course {
    private String instructorName;
    private String location;
    private String classTime;

    public void setInstructorName(String instructor) {
        this.instructorName = instructor;
    }

    public String getInstructorName() {
        return this.instructorName;
    }

    public void setLocation(String loc) {
        this.location = loc;
    }

    public String getLocation() {
        return this.location;
    }

    public void setClassTime(String time) {
        this.classTime = time;
    }

    public String getClassTime() {
        return this.classTime;
    }

    @Override
    public void printInfo() {
        super.printInfo();
        System.out.println("   Instructor Name: " + getInstructorName());
        System.out.println("   Location: " + getLocation());
        System.out.println("   Class Time: " + getClassTime());
    }
}
