# MaxMinEmployeeSalary

package demp.java.maxminemployee;

import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class EmployeeMaxMain {
	
	public static void main(String args[]) {
		
		List<Employee> refList = new ArrayList();
		refList.add(new Employee(101,"James1","Dev1", 10.20));
		refList.add(new Employee(102,"James2","Dev2", 50.10));
		refList.add(new Employee(103,"James3","Dev3", 30.90));
		refList.add(new Employee(104,"James4","Dev4", 70.40));
		refList.add(new Employee(105,"James5","Dev5", 20.50));
		
		// Alternatively we can find it by using Collections.max() method.
		Collections.sort(refList,(emp1,emp2)-> Double.compare(emp1.getEmp_sal(), emp2.getEmp_sal()));
		System.out.println("Employee with the Higest Salary : "+refList.get(refList.size()-1));
		
		Employee refEmployee = Collections.min(refList,(emp1,emp2)-> Double.compare(emp1.getEmp_sal(), emp2.getEmp_sal()));
		System.out.println("Employee with the Minimum Salary : "+refEmployee);
		
	}

} // end of EmployeeMaxMin

============================================================================================================================



package demp.java.maxminemployee;

public class Employee {

	int emp_number;
	String emp_name;
	String emp_dept;
	double emp_sal;
	
	public Employee(int emp_number, String emp_name, String emp_dept, double emp_sal) {
		super();
		this.emp_number = emp_number;
		this.emp_name = emp_name;
		this.emp_dept = emp_dept;
		this.emp_sal = emp_sal;
	}
  
	public int getEmp_number() {
		return emp_number;
	}
	public void setEmp_number(int emp_number) {
		this.emp_number = emp_number;
	}
	public String getEmp_name() {
		return emp_name;
	}
	public void setEmp_name(String emp_name) {
		this.emp_name = emp_name;
	}
	public String getEmp_dept() {
		return emp_dept;
	}
	public void setEmp_dept(String emp_dept) {
		this.emp_dept = emp_dept;
	}
	public double getEmp_sal() {
		return emp_sal;
	}
	public void setEmp_sal(double emp_sal) {
		this.emp_sal = emp_sal;
	}
	@Override
	public String toString() {
		return "Employee [emp_number=" + emp_number + ", emp_name=" + emp_name + ", emp_dept=" + emp_dept + ", emp_sal="
				+ emp_sal + "]";
	}

	
} // end of Employee class


===========================================================================================================================

Output:

Employee with the Higest Salary : Employee [emp_number=104, emp_name=James4, emp_dept=Dev4, emp_sal=70.4]
Employee with the Minimum Salary : Employee [emp_number=101, emp_name=James1, emp_dept=Dev1, emp_sal=10.2]

