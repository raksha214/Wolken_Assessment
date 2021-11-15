package com.example.serve.controller;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.data.repository.query.Param;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RestController;

import com.example.serve.BalanceController;
import com.example.serve.dto.EmployeeDTO;
import com.example.serve.service.EmployeeService;
import com.example.serve.entity.EmployeeEntity;
@RestController
public class EmployeeController {
Logger logger = LoggerFactory.getLogger(BalanceController.class);
	
	@Autowired
	EmployeeService service;
	
	@PostMapping("findEmployee")
    String save(@RequestBody EmployeeDTO dto) {
	String msg = null;
	try {
		logger.info(""+dto);
		msg = service.validateAndSave(dto);
		
	} catch(Exception e) {
		logger.error(e.getMessage());
	}
	
	return msg;
}
	
	@PostMapping("saveEmployee")
    String saveALL(@RequestBody EmployeeDTO dto) {
	String msg = null;
	try {
		logger.info(""+dto);
		msg = service.validateAndSave(dto);
		
	} catch(Exception e) {
		logger.error(e.getMessage());
	}
	
	return msg;
}
	
	@PostMapping("saveAllEmployees")
	String saveAllEmployeeDetails(@RequestBody List<EmployeeDTO> dtos) {
		String ret = service.validateAndSaveAll(dtos);
		log.info("saveAllEmployeeDetails");
		return ret;
	}
	
	@PostMapping("findByDesignation")
    EmployeeDTO getByDesignation(@Param(value="designation") String designation) {
	EmployeeDTO dto = null;	
		try {
              logger.info(designation);			
			  dto = service.validateAndFindByDesignation(designation);		
		} catch(Exception e) {
			logger.error("========");
			logger.error(e.getMessage(), e.getClass());
		}
		return dto;
	}
	
	
	@PostMapping("findBySalary")
    EmployeeDTO getByDesignation(@Param(value="salary") float salary) {
	EmployeeDTO dto = null;	
		try {
              //logger.info(salary);			
			  dto = service.validateAndFindBySalary(salary);		
		} catch(Exception e) {
			logger.error("========");
			logger.error(e.getMessage(), e.getClass());
		}
		return dto;
	}
	
	}
