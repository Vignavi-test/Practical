HeroVired Capstone project

Group 1 : Jyothi Gutta (Github link : https://github.com/jyothigutta) & Harimedha K (https://github.com/Harimedha)



Create a Job portal website where:
 A candidate will:
	Create account
		> Email
		> Password
	Login
 
	Add details in profile like
		> Phone number
		> Current company
		> Current CTC
		> Current role
		> About
		> Profile picture
		> Upload CV
		> Add skills
		
	View the list of jobs
	
	Refer Figma design for the information		
		Apply in those jobs
	
	Figma Design:

	https://www.figma.com/file/VhTa9EH1FxszIjiVr7xc8u/Jobs?nodeid=0%3A1&t=jYeEhjrdIXVKF4Ak-3
	
	
Tech expectation:

	Frontend: React
	Backend: Ruby on Rails
	Database: PostgreSQL



Backend tasks 


1. Create new rails project
	
		> rails new jobportal -d postgresql

2. Configuring the database.yml
			Setting databasename:<dbname>
					postgresuser:<postgreuesr>
					password	:<password>
					host		:<localhost>

3. Installation of bcrypt gem
			Add "gem brcypt" in Gemfile

4. Creation of migration files for respective tables:
	
		> rails db migration create_candidateapplication		
		> rails db migration create_candidatejob
		> rails db migration create_candidateprofile
		> rails db migration create_jobdetail
		> rails db migration create_job
		> rails db migration create_user

	DB Schema:
		
			  create_table "candidateapplications", force: :cascade do |t|
				t.integer "userid"
				t.string "jobcode"
				t.date "applieddate"
				t.string "candidateapplicationstatus"
				t.string "location"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
				t.integer "jobid"
			  end

			  create_table "candidatejobs", force: :cascade do |t|
				t.string "jobcode"
				t.string "applicationstatus"
				t.string "appliedon"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
				t.integer "candidateid"
			  end

			  create_table "candidateprofiles", force: :cascade do |t|
				t.string "firstname"
				t.string "lastname"
				t.string "email"
				t.string "contact"
				t.string "address"
				t.string "about"
				t.string "profilepic"
				t.string "company"
				t.integer "ctc"
				t.integer "experience"
				t.string "role"
				t.string "skills"
				t.string "resumelink"
				t.integer "expectedsalary"
				t.string "preferedlocation"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
			  end

			  create_table "jobdetails", force: :cascade do |t|
				t.string "jobtitle"
				t.string "jobdescription"
				t.string "companyname"
				t.string "jobtype"
				t.string "location"
				t.integer "salary"
				t.date "posteddate"
				t.string "domain"
				t.string "jobcode"
				t.string "skillsrequired"
				t.string "applicationstatus"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
			  end

			  create_table "jobs", force: :cascade do |t|
				t.string "title"
				t.string "description"
				t.string "location"
				t.string "jobtype"
				t.string "salary"
				t.string "company"
				t.string "domain"
				t.string "jobcode"
				t.string "skills"
				t.date "posted_on"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
			  end

			  create_table "users", force: :cascade do |t|
				t.string "email"
				t.string "password_digest"
				t.datetime "created_at", null: false
				t.datetime "updated_at", null: false
			  end


5. Generated respective Models for tables for adding constraints
	
		> Candiateapplication.rb
		> Candidatejobs.rb
		> candidateprofile.rb
		> jobdetail.rb
		> jobs.rb
		> user.rb
		
	
6. Created of controllers for APIs

	> rails db migration create_candidateapplication		
		> rails generate controller candidatejob
		> rails generate controller	candidateprofile
		> rails generate controller jobdetail
		> rails generate controller job
		> rails generate controller	user		
		> rails generate controller	login
		> rails generate controller	logout
		> rails generate controller	jobsbystatus
		> rails generate controller	user
		> rails generate controller	profilebyemail
		
		
Frontend Tasks:

React Components:

Creating react application:
	
	> npx create-react-app jobportal
	
Installation of required library
	
	> npm install react-router-dom
	
	> npm install axios
	
React Components creation

	> Login 
	> Profile Page
	> Header
	> AllJobs
	> Eligible Jobs
	> Applied Jobs
	> Shortlisted Jobs
	> Interviewing Jobs
	> Rejected Jobs
	> Offer received Jobs
	
Reused components
	> Searchboxcontainer
	> Dropdown
	> JobCard
	> Snapshotcard
	> JobPostingCard



	
