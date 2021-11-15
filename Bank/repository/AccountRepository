package com.example.serve.repository;
import java.util.List;
import org.springframework.data.jpa.repository.support.JpaRepositoryImplementation;
import com.example.serve.entity.AccountEntity;

public interface AccountRepo extends JpaRepositoryImplementation<AccountEntity, Integer>{
	List<AccountEntity> getAccountByBranchName(String branchName);
	AccountEntity getByAccNo(int accNo);
  AccountEntity getAmountByAccHolderName(String name);
}
