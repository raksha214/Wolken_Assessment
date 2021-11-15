package com.example.serve.entity;

import java.util.Date;

import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.Id;
import javax.persistence.Table;

import org.hibernate.annotations.GenericGenerator;

import lombok.Getter;
import lombok.NoArgsConstructor;
import lombok.Setter;
import lombok.ToString;
@Getter
@Setter
@NoArgsConstructor
@ToString
@Entity
@Table

public class AccountEntity {
  @Id
	@GenericGenerator(name="acc", strategy="increment")
	@GeneratedValue(generator="acc")
	private int accNo;
	private String accHolderName;
	private long contact;
	private String email;
	private String address;
	private String branchName;
	private String Type;
	private float amount;
	private boolean status;
	private String nominee;
	private String gender;
	private Date dob;
}
