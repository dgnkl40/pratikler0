public class Course {
    Teacher teacher;
    String name;
    String code;
    String prefix;
    int note;
    int noteS;

    Course(String name,String code,String prefix,Teacher teacher){
        this.teacher = teacher;
        this.name = name;
        this.code = code;
        this.prefix = prefix;
        int note ;
        int noteS;

    }
    void addTeacher(Teacher teacher){
        this.teacher = teacher;
        printTeacherİnfo();
    }
    void printTeacherİnfo(){
        this.teacher.print();
    }

}

public class Teacher {
    String name;
    String branch;
    String mpno;

    Teacher(String name,String mpno,String branch){
        this.name = name;
        this.branch =  branch;
        this.mpno = mpno;

    }
    void  print(){
        System.out.println("Adı: " + this.name);
        System.out.println("Branşı: " + this.branch);
        System.out.println("Numara: " + this.mpno);

    }
}
public class Student {
    String name;
    String stuNo;
    String classes;
    Course course1;
    Course course2;
    Course course3;
    Course note1S;
    Course note2S;
    Course note3S;
    double avarage;
    boolean isPass;

    Student(String name,String stuNo,String classes,Course course1,Course course2,Course course3, Course note1S, Course note2S, Course note3S){
        this.name = name;
        this.stuNo = stuNo;
        this.classes = classes;
        this.course1 = course1;
        this.course2 = course2;
        this.course3 = course3;
        this.note1S = note1S;
        this.note2S = note2S;
        this.note3S = note3S;
        this.avarage = 0.0;
        this.isPass = false;

    }
    void addBulkExamNote(int note1,int note2,int note3,int note1S,int note2S,int note3S) {
        if (note1 >= 0 && note1 <= 100) {
            this.course1.note = note1;
        }
        if (note2 >= 0 && note2 <= 100){
            this.course2.note = note2;
    }
        if (note3 >= 0 && note3 <= 100) {
            this.course3.note = note3;

        }
        if (note1S >= 0 && note1S <= 100) {
            this.note1S.noteS = note1S;

        }
        if (note2S >= 0 && note2S <= 100) {
            this.note2S.noteS = note2S;

        }
        if (note3S >= 0 && note3S <= 100) {
            this.note3S.noteS = note3S;

        }

    }
    void isPass(){
        System.out.println("=============================");
        this.avarage = (((course1.note +  course2.note + course3.note)*0.8) +((note1S.noteS + note2S.noteS + note3S.noteS)*0.2))/3.0;
        if (this.avarage >= 55){
            System.out.println("#Sınıfı Geçtin#");
        }else {
            System.out.println("#Kaldın#");
        }printNote();
    }
    void printNote(){

        System.out.println(course1.name + " Notu: " + this.course1.note);
        System.out.println(course2.name + " Notu: " + this.course2.note);
        System.out.println(course3.name + " Notu: " + this.course3.note);
        System.out.println(course1.name + " Sözlü Notu: " + this.note1S.noteS);
        System.out.println(course2.name + " Sözlü Notu: " + this.note2S.noteS);
        System.out.println(course3.name + " Sözlü Notu: " + this.note3S.noteS);
        System.out.println("Ortalama: " + this.avarage);
    }

}
public class Mainn {
    public static void main(String[] args) {
        Teacher t1  =new Teacher("Kutluhan KORKMAZ" , "55555","TRH");
        Teacher t2 = new Teacher("Sabri DOĞAN","55554","BİO");
        Teacher t3 = new Teacher("Buse AkKAYA","55553","MAT");

        Course tarih = new Course("TARİH","111","TRH",t1);
        Course bio = new Course("BİYOLOJİ","222","BİO",t2);
        Course mat = new Course("MATEMATİK","333","MAT",t3);


        Course note1S = new Course("TARİH","111","TRH",t1);
        Course note2S = new Course("BİYOLOJİ","222","BİO",t2);
        Course note3S = new Course("MATEMATİK","333","MAT",t3);

        Student s1 = new Student("Ökkeş","11","4",tarih,bio,mat,note1S,note2S,note3S);
        s1.addBulkExamNote(87,55,89,45,72,36);
        s1.isPass();
        Student s2 = new Student("Şerife","22","3",tarih,bio,mat,note1S,note2S,note3S);
        s2.addBulkExamNote(10,78,53,78,52,90);
        s2.isPass();
        Student s3 = new Student("Mükremin","33","2",tarih,bio,mat,note1S,note2S,note3S);
        s3.addBulkExamNote(46,60,32,80,71,83);
        s3.isPass();
    }

}
