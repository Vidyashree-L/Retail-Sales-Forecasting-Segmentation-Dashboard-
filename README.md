code:

form customer_segment_assignments
{
	displayname = "Customer Segment Assignments"
	success message = "Data Added Successfully!"
	Section
	(
		type = section
	 	row = 1
	 	column = 0   
		width = medium
	)
	customer
	(
		type = picklist	
		displayname = "Customer"
		values  = leads.ID
    	displayformat = [title]
		allow new entries
		[
			displayname = "Add New"
		]
		sortorder = ascending
	 	row = 1
	 	column = 1   
		width = medium
	)
	segment
	(
		type = list	
		displayname = "Segment"
		values  = customer_segments.ID
    	displayformat = [segment_id]
		allow new entries
		[
			displayname = "Add New"
		]
		sortorder = ascending
		height = 13px
	 	row = 1
	 	column = 1   
		width = medium
	)
	assignment_date
	(
    	type = date
		displayname = "Assignment Date"
		alloweddays = 0,1,2,3,4,5,6
	 	row = 1
	 	column = 1   
		width = medium
	)
	confidence_score
	(
    	type = percentage
		displayname = "Confidence Score"
		maxchar = 16
	 	row = 1
	 	column = 1   
		width = medium
	)
	reason
	(
    	type = text
		displayname = "Reason"
	 	row = 1
	 	column = 1   
		width = medium
	)
	
	actions
	{
		on add
		{
			submit
			(
   				type = submit
   				displayname = "Submit"
			)
			reset
			(
   				type = reset
   				displayname = "Reset"
			)
		}
		on edit
		{
			update
			(
   				type = submit
   				displayname = "Update"
			)
			cancel
			(
   				type = cancel
   				displayname = "Cancel"
			)
		}
	}
	blueprint components
	{
		stages = {"Assignment Created","Segment Assigned","Review Required","Assignment Cancelled","Assignment Rejected","Assignment Verified","Assignment Reassigned","Assignment Finalized","Assignment Monitored","Assignment Updated"}
	}
}

Problem Statement
Analyze retail sales data to identify trends,
customer segments and business opportunities.
Technologies
Python
Pandas
SQL
Streamlit
Power BI
Tableau
OpenPyXL
Features
✔ EDA
✔ Feature Engineering
✔ Customer Segmentation
✔ KPI Dashboard
✔ Excel Report Automation
✔ Interactive Filters

#Results

Processed 9,994 transactions
Built 10+ KPI dashboard
Automated reporting
Saved 5+ hours/week

<img width="1600" height="698" alt="image" src="https://github.com/user-attachments/assets/4ca8248a-d46e-4781-803b-81d76336fc04" />

<img width="1600" height="699" alt="image" src="https://github.com/user-attachments/assets/b88ee502-1038-47dd-8f8a-d6f6b3cff370" />


