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
