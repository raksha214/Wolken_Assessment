package com.example.serve.service;

import java.util.ArrayList;
import java.util.List;

import org.hibernate.TypeMismatchException;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.BeanUtils;
import org.springframework.beans.factory.annotation.Autowired;

import com.example.serve.dto.EmployeeDTO;
import com.example.serve.entity.EmployeeEntity;
import com.example.serve.repository.EmployeeRepo;



public class EmployeeServiceImpl implements EmployeeService{

	@Autowired
	EmployeeRepo repo;
  
  private Logger log = LoggerFactory.getLogger(this.getClass());

@Autowired
EmployeeRepo repo;

@Override
public String validateAndSave(EmployeeDTO dto) {
	try {
		if(dto!=null) {
			EmployeeEntity entity = new EmployeeEntity();
			BeanUtils.copyProperties(dto, entity);
			repo.save(entity);
			return "Data Saved Successfully";
		}
		else {
			log.info("DTO is null");
		}
	} catch (NullPointerException | TypeMismatchException e) {
		log.error(e.getMessage(), e.getClass().getSimpleName());
	}
	return null;
}

@Override
public String validateAndSaveAll(List<EmployeeDTO> dtos) {
	String out=null;
	for (EmployeeDTO dto : dtos) {
		if(dto!=null) {
			out = validateAndSave(dto);
		}
		else {
			log.info("DTO List is null");
		}
	}
	return out;
}


@Override
public List<EmployeeDTO> validateAndFindAll() {
	List<EmployeeEntity> entityList = repo.findAll();
	List<EmployeeDTO> dtos = new ArrayList<>();
	log.info(""+entityList);
	for (EmployeeEntity employeeEntity : entityList) {
		EmployeeDTO dto = new EmployeeDTO();
		BeanUtils.copyProperties(employeeEntity, dto);
		dtos.add(dto);
	}
	log.info(""+dtos);
	return dtos;
}


@Override
public List<EmployeeDTO> validateAndFindByDesignation(String designation) {
	List<EmployeeEntity> entityList = repo.findByDesignation(designation);
	List<EmployeeDTO> dtos = new ArrayList<>();
	log.info(""+entityList);
	for (EmployeeEntity entity : entityList) {
		EmployeeDTO dto = new EmployeeDTO();
		BeanUtils.copyProperties(entity, dto);
		dtos.add(dto);
	}
	log.info(""+dtos);
	return dtos;
}

@Override
public List<EmployeeDTO> validateAndFindBySalary(float salary) {
	List<EmployeeEntity> entityList = repo.findBySalary(salary);
	List<EmployeeDTO> dtos = new ArrayList<>();
	log.info(""+entityList);
	for (EmployeeEntity entity : entityList) {
		EmployeeDTO dto = new EmployeeDTO();
		BeanUtils.copyProperties(entity, dto);
		dtos.add(dto);
	}
	log.info(""+dtos);
	return dtos;
}

}
