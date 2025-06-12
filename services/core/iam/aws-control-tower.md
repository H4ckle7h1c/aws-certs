Purpose : 
- Allow quick & easy setup of multi account envs.
- Orchastrates other services to provide this functionnality
- Org, IAM Identity Center, CloudFormation,... 
- SSO/ID Federation, Centralized logging & Auditing (CW, CT, SNS,...)
- Org dashboard 
Definition : 


Key Concepts :
- Landing Zone - multi account env
- Guard Rails : Detect / Mandatate rules accross accounts
- Account Factory : automates and standardized acc creation

When CT created in an account : 
- account becomes the landing zone mgt account
- 2 OU :
	- functional (security) : 2 AWS accounts are created :
		-  archive:  like CT + aws config
		+ audit : SNS, CW
	- custom (sandbox)

	It can be seen as an Account Factory :
		- Use Cloud Formation  in order to create provisioned accounts with templates
		- Take advantage of SCP + Config = Guardrails to detect drifts 
 ![[Pasted image 20250612094045.png]]

- Landing zone :
	- Home region -> original region in which the product is deployed 
Guardrails : 
- Rules for multi-account governance
- Mandatory, strongly-recommended or elective rules
- Preventive : stop doing things (SCP)
	- Rules are enforces or not enabled
	- allow, deny regions,...
- Detective : config checks (AWS config)
	- clear, in violation, not enabled
	- e.g. detect cloudtrail enabled 

Account factory :
- Automated provisioning 
- created by end users or admins 
- guardrails automatically added 
- account admin given to a named user (IAM Center)
- config with account & network standard conf 
- accounts can be closed or repurposed
- integrated into business SDLC