public class Company {
									
								//   Att
	private String name;
	private Employee [] arrEmps;
	private int nbEmps;
	
								//   Temp
	int nbM = 0;
	int nbE = 0;
	
	public Company(String name, int size)
	{
		this.name = name;
		arrEmps = new Employee[size];
		nbEmps = 0;
	}
	
	public boolean addEmployee(Employee e)
	{
		if(nbEmps < arrEmps.length){
			if(e instanceof Manager)
				arrEmps[nbEmps++] = new Manager((Manager)e);
			else if(e instanceof Consultant)
					arrEmps[nbEmps++] = new Consultant((Consultant)e);
				else
					arrEmps[nbEmps++] = new Employee(e);
			
		return true;}
		return false;
	}
  
  }
