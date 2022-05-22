# Linx-Api-Server

1.Implement the getFeedback operation of the Assess service.
a.If sNR matches your own student number, return a sentence of your choice for feedback.
b.If sNR does not match your student number, return “student number not found”.

2.Implement the submit operation of the Assess service, which should use the checkFile operation of the File service to verify the URL and return the submission details in JSON format (not the file) as a confirmation to the student. Please adhere to the JSON schema for Submission objects provided on BlackBoard.
a.If sid matches your university account name (your email address up to but not including @), then
i.If url matches an existing URL on the File service, return a JSON object of type Submission with the values of module, assessment and URL fields copied from the corresponding input parameters.
ii.If url does not match an existing URL on the File service, return Submission object with subNr = “no such file”.
b.If sid does not match your university account name, return Submission object with subNr = “no such user”.

3.To tests the submit operation, create three REST-specific sequence diagrams describing the execution of test cases with their concrete inputs and outputs covering cases a.i, a.ii and b in Task 2 above. You will have to include an invocation of upload() on the File service before being able to test your submit() operation.  
