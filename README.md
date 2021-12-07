****DOCTOR****
/**
 * 
 */

/**
 * @author Chand
 *
 */
public class Doctor extends HospitalEmployee {
	String Specialty;

	public Doctor(String name, int number, String specialty) {
		super(name, number);
		Specialty = specialty;
	}

	@Override
	public String toString() {
		return "" + getName() + " " + getNumber() + " " + Specialty + ".";
	}

	public void work() {
		System.out.println(getName() + " works for the hospital. "+ getName() +" is a(n) Heart doctor.");
	}

}

****HOSPITAL****

//********************************************************************
//  Hospital.java       Authors: Lewis/Loftus
//
//  Solution to Programming Project 9.2 
//********************************************************************

public class Hospital
{
   //-----------------------------------------------------------------
   //  Creates several objects from classes derived from
   //  HospitalEmployee.
   //-----------------------------------------------------------------
   public static void main (String[] args)
   {
      HospitalEmployee vito = new HospitalEmployee ("Vito", 123);
      Doctor michael = new Doctor ("Michael", 234, "Heart");
      Surgeon vincent = new Surgeon ("Vincent", 645, "Brain", false);
      Nurse sonny = new Nurse ("Sonny", 789, 6);
      

      // print the employees
      System.out.println (vito);
      System.out.println (michael);
      System.out.println (vincent);
      System.out.println (sonny);
      

      // invoke the specific methods of the objects
      vito.work();
      michael.work();
      vincent.work();
      sonny.work();
     
   }
}

*****HOSPITAL EMPLOYEE****


/**
 * 
 */

/**
 * @author Chand
 *
 */
public class HospitalEmployee {
	protected String name;
	protected int number;

	public HospitalEmployee(String name, int number) {
		super();
		this.name = name;
		this.number = number;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public int getNumber() {
		return number;
	}

	public void setNumber(int number) {
		this.number = number;
	}

	@Override
	public String toString() {
		return "" + name + " " + number + ".";
	}

	public void work() {
		System.out.println(name + " works for the hospital.");
	}
}

******NURSE*****


/**
 * 
 */

/**
 * @author Chand
 *
 */
public class Nurse extends HospitalEmployee {
	int numOfPatients;

	public Nurse(String name, int number, int numOfPatients) {
		super(name, number);
		this.numOfPatients = numOfPatients;
	}

	@Override
	public String toString() {
		return "" + getName() + " " + getNumber() + " " + numOfPatients + ".";
	}

	public void work() {
		System.out.println(getName() + " works for the hospital. "+ getName() +" is a nurse with "+ this.numOfPatients +" patients.");
	}
}

****SURGEON****


/**
 * 
 */

/**
 * @author Chand
 *
 */
public class Surgeon extends HospitalEmployee {
	 String Operating ;
	 Boolean True  ;
	
	

	public Surgeon(String name, int number,String operating, Boolean true1) {
		super (name,number);
		Operating = operating;
		True = true1;
	}

	@Override
	public String toString() {
		return ""+getName()+ " "+ getNumber()+" " + Operating + " Operating : "  +  True + ".";
	}

	public void work() {
		System.out.println (getName() + " works for the hospital. "+ getName() +" is operating now.");		
	}

}
