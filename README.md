# Construction-Maintenance-Cell


## Login on gne12.gndec.ac.in

## Go to Company list

### Parent company - Nanakana Sahib Educational Trust

1. Set Guru Nanak Dev Engineering College
2. Set Guru Nanak Polytechnical College
3. Construction and Maintenance Cell and set domain Services


## Create Doctype Maintenance Request

Set fields according to therir needs like - subject, Nature of work, Details of required work etc.

After this Create its web form this process is very simple.

## Create Estimante doctype and set its feilds.

And connect with the Maintenance request and it shows only SDO.

# Workflow :

1. Create doctype of “Maintenance Request” in which request will sent through a webform of required fields.

2. Go to workflow in ‘Build’ domain and and new workflow.

3. Set the name of workflow as “Construction and Maintenance Request Approval” and under document type field, fill “Maintenance Request”

4. Now swipe up a little and under the states, create new first state as “Draft”, Doc Status=0 and under “allow only edit for” column, create new role here naming “CMC User” and then select it.

5. Create second state naming “Justification Needed”, with doc status=0 and allow only edit for “CMC User” role.

6. Create third state naming “Forwarded by HOD”, with doc status=0 and create role as “HOD” under allow only edit for.

7. Same way, create fourth state and name it as “Forwarded by SDO”, with doc status=0 and allow only to edit for “SDO”.

8. Create next state “Approved” with doc status=1 and allow only edit for “CMC Authority”.

9. Create next state “Rejected” with doc status=2 and allow only to edit for “Rejector” (Need to create new role here i.e. “Rejector”

9. Now under “Transition Rules”, add first rule under “State” column, select “Draft”, under “Action” column add new action naming “Forward”, under “Next State” select “Forwarded by HOD” and under “Allowed” column, select “HOD”.

10. In the same way, add second rule by selecting state as “Draft”, create new action as “Need Justification”. Select next state as “Justification needed” and allowed to 'HOD’.

11. Add third rule by selectiong state as “Draft”, create action “Reject”, next state as “Rejected”, which is also allowed to HOD here.

12. Now add next rule by selecting state as “Forwarded by HOD”, create new action as “Accept with estimate”, Next state as “Approved” and allowed to SDO role.

13. Add next by selecting again as “Forwarded by HOD”, create new action as “Forward with Estimate”, next state as “Forwarded by SDO”, and allowed to SDO again.

14. Add more rule by selecting state as “Forward by HOD”, select action “Reject”, next state as “Rejected”, allowed to SDO one more time.

15. In the same way, next rule is selecting state as “Forwarded by SDO”, select action as “Approve”, next state as “Approved” and allowed to “Office Incharge” by creating new role here.

16. Now in the last rule, select state as “Forward by SDO” again, select action “Reject”, next state as “Rejected” which will also allowed to Office Incharge.

Now, the only thing left is to assign the roles like SDO, Office Incharge, HOD and CMC Aurhority (to both SDO and O/incharge) and Rejector (to HOD, SDO and O/incharge) with corresponding to their login credentials.




# Here everyone add further your documentation related to their tasks.

Fork it make changes and send PR .

All the best Guys.
