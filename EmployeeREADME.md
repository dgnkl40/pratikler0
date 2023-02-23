public class Employee {
    String name;
    double salary;
    int workHours,hireYears;

    Employee(int hireYears,int workHours,double salary,String name){
        this.name = name;
        this.salary = salary;
        this.workHours = workHours;
        this.hireYears = hireYears;

    }
    double tax(){
        if (this.salary >=1000){
            return this.salary * 0.03;
        }
        return 0.0;
    }
    double bonus(){
        return (this.workHours - 40 ) * 30;
    }
    double raiseSalary() {
        int years = 2023 - hireYears;
        if (years < 10) {
            return this.salary * 0.05;
        }
        else if (years >= 10 && years < 20) {
            return this.salary * 0.1;

        } else  {
            return this.salary * 0.15;

        }


        }
        public String toString() {
            System.out.println("=================================");
            System.out.println("Ad ve Soyad : " + this.name);
            System.out.println("Maaş : " + this.salary);
            System.out.println("Başlama Yılı : " + this.hireYears);
            System.out.println("Vergi : " + this.tax());
            System.out.println("Çalışma Saati : " + this.workHours);
            System.out.println("Bonus : " + this.bonus());
            System.out.println("Maaş Artışı : " + this.raiseSalary());
            double total1 = this.salary - this.tax() + this.bonus();
            System.out.println("Vergi ve Bonusla Birlikte Maaş : " + total1);
            System.out.println("Toplam Maaş: " + (this.salary + this.raiseSalary()));
            return getClass().getName() + "@" + Integer.toHexString(hashCode());
        }
    }

public class Fabric {
    public static void main(String[] args) {
        Employee e1 = new Employee(1985,45,2000,"Buse Akkaya");
       e1.toString();

       Employee e2 = new Employee(1995,50,2500,"Doğan Kul");
       e2.toString();

       Employee e3 = new Employee(2000,43,1500,"Ali Veli");
       e3.toString();

    }


}
