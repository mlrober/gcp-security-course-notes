# gcp-security-course-notes

GCP Professional Security Course

Regions & ZOnes
Zones
	- Independent Physical Data Center
Regions
	- Different Geographical Area
Regions can contain multiple zones
Multi Regions - Collection of Regions
Global (World)
	Multi Regions (Diff. Countries like India, Russia, Cuba)
		Region (India)
			Zone (India-South, India-East)
currently 25 Regions and 76 Zones available
Nomenclature of Regions
If -a or -b in name, it represent Zones
Ex. Asia-South1-a, Asia-South1-b etc. 
If ends like Asia-South1, it represents a region

GCP Services
	- 200 Services in GCP

Overview
User Management
- Google Account Authentication - Support SAML
- Enforce Rule
- Password Length, 2 Step Verification
Storage Data
- By Default, all data is encrypted with Google Managed Encryption Key
- CMEK, CSEK
Data in Transit
- By defautl, All data encrypts when goes out of beyond google environment
Google IAP
- Secure Appengine, VM access
DLPrevention (DLP)
- Inspect
- Redact
- Transform
- Re-identify PII Data
VPC Security
- Subnet
- Firewall Rules
- Ingress/Egress Traffic
- Cloud Armor
Operations
- Logging
- Monitoring
- Tracking
- Labelling

Shared Responsibility Model
Cloud Identfy
- 5 Ways of Cloud Identify
	- GAccount
		- Individual/Single Account
		- Doesn't Suite for managing Porjects
	- SA
	- Gworkspace (Gsuite)
		- Allows to manage multiple users with organizational features
		- It has all products of gcloud like sheets, docs and other
	- GIdentity Domain
		- Similar to workspace without gapps
		- Organizational User Management

		- Multiple Users can be attached with central control
	- Ggroups
- Password Strength
	- Minimum 8 to 100 characters
-GCDS
	- Gcloud Directory Sync
		- It allows to sync data in Ms AD or ldap into gidentity
		- It will aloow users in Microsoft or onPrem AD or Ldap to sync with glcoud and use gidentity without ldap
		- Simply, It will sync all data in ldap or AD and allow users to use gidentity instead of onprem AD or Ldap for authentication or login
- Organizatin Policies
	- 3 Types of Policies
		- Disable Service Account Creation
		- Enforce Uniform Bucket Level Access
		- Skip Default Network Creation
- There are 3 types of roles
- Primitive
	- Basic Role where it is limited to project only and it can apply to project and not to any other
	- Provides Broader Access to all resources inside the project
	- E.g. if user is owner, he can edit/delte any resource in the project
	- E.g. If write access, he can write to any reource in project
	- It doesn't follow principle of least privileges
	- It has Owner, Editor, Viewer only
- Predefined
	- It is applicable only for a single service and doesn't apply to all
	- these are depends on the service and are service specific roles
	- E.g, Compute Admin, Network Viewer, BigQuery Job User
- Custom Role
	- Customized roles where some permissions from previous can be inherited to create
	
