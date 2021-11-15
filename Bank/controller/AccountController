package com.example.serve.controller;

import java.util.List;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.data.repository.query.Param;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

import com.example.serve.dto.AccountDto;
import com.example.serve.dto.EmployeeDto;
import com.example.serve.entity.AccountEntity;
import com.example.serve.service.AccountService;

@RestController
public class AccountController {
	private Logger logger=LoggerFactory.getLogger(this.getClass());
	@Autowired
	AccountService service;
	@PostMapping("saveAccount")
	String save(@RequestBody AccountDto dto)
	{
		String message=null;
		try {
			message=service.validateAndSave(dto);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return message;
	}

  @PostMapping("deposit")
	String deposit(@RequestParam int accNo,float amount)
	{
		String message=null;
		try {
			message=service.validateAndDepsoit(accNo,amount);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return message;
	}
	
	@GetMapping("getAccountByBranchName")
	List<AccountDto> getAccountByBranchName(@RequestParam String branchName)
	{
		List<AccountDto> dto=null;
		try {
			dto=service.validateAndGetAccountByBranchName(branchName);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return dto;
	}
	@GetMapping("getAllAccount")
	List<AccountDto> getAllAccount()
	{
		List<AccountDto> dto=null;
		try {
			dto = service.validateAndGetAllAccount();
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return dto;
	}
  @GetMapping("getAmountByAccHolderName")
	String getAmountByAccHolderName(@RequestParam String name)
	{
		String dto=null;
		try {
			dto=service.validateAndGetBalanceByName(name);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return "Balance:"+dto;
	}
  @PostMapping("statusUpdate")
	String statusUpdate(@RequestParam int accNo)
	{
		String message=null;
		try {
			message=service.validateAndUpdateStatus(accNo);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return message;
	}
	@PostMapping("withdraw")
	String withdraw(@RequestParam int accNo, float amount)
	{
		String message=null;
		try {
			message=service.validateAndWithdraw(accNo,amount);
		} catch (Exception e) {
			logger.info(e.getMessage(),e.getClass().getName());
		}
		return message;
	}
}
