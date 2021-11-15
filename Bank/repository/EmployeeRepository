package com.example.serve.repository;
import java.util.List;

import org.springframework.data.jpa.repository.JpaRepository;
import com.example.serve.entity.EmployeeEntity;
public interface EmployeeRepo extends JpaRepository<EmployeeEntity,Integer>{

	List<EmployeeEntity> findByDesignation(String designation);
	List<EmployeeEntity> findBySalary(float salary);

}
