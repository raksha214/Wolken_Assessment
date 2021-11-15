package com.example.serve.entity;

import javax.persistence.Entity;
import javax.persistence.Id;
import javax.persistence.GeneratedValue;
import lombok.Getter;
import lombok.NoArgsConstructor;
import lombok.Setter;
import org.hibernate.annotations.GenericGenerator;

@Getter
@Setter
@NoArgsConstructor
@Entity
public class EmployeeEntity {
	
	@Id
	@GenericGenerator(name = "athul" , strategy="increment")
	@GeneratedValue(generator="athul")
	private int id;
	private String name;
	private String deignation;
	private float salary;
	private long contactNumber;
	private String email;
	

}
