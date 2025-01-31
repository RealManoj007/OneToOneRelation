in one to one relation

do not save object of child in parent and first save parent and give in parent, chdild field cascade, so that first they will save as soon as parent.repo is going to save.
Here Pen is parent
Mobile and Emp are child

    Pen pen=new Pen();
		pen.setPenName("Parker");


		Emp emp=new Emp();
		emp.setEmpName("Rahul");
		emp.setPen(pen);

		Mobile mob=new Mobile();
		mob.setMobileName("Samsung");
		mob.setPen(pen);

//		pen.setPenEmp(emp);   do not save child object in parent, bcoz we won't needed to shown in parent, data will display in child
//		pen.setPenMob(mob);
		penRepo.save(pen);
		empRepo.save(emp);
		mobileRepo.save(mob);

![image](https://github.com/user-attachments/assets/770edeee-7e49-412d-82a5-38b4ef94822a)
