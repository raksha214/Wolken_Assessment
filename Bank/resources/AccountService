package com.example.serve.service;
import java.util.List;
import com.example.serve.dto.AccountDto;

public interface AccountService {

	String validateAndSave(AccountDto dto);
  List<AccountDto> validateAndGetAllAccount();
	String validateAndGetBalanceByName(String name);
  List<AccountDto> validateAndGetAccountByBranchName(String branchName);
  String validateAndDepsoit(int accNo, float amount);
  String validateAndWithdraw(int accNo, float amount);
  String validateAndUpdateStatus(int accNo);

}
