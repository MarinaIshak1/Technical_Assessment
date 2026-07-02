**Envelope ID for task 1 "05702bcc-706a-8a79-8005-6e8f857c01d0"**,

**Envelope ID for task 3 "0d552452-63c0-8a7b-80e5-c8663179014e"**,

**Envelope ID for task 4  "112022a0-5cf2-8636-8133-26b1007c0145"**



**Task 1 response**

"Hi,

We're sorry to hear you're experiencing this issue.

After reviewing the document, we noticed that it is a dynamic PDF containing interactive form fields. We recommend printing the document to PDF and saving the printed version. This process will flatten the existing form fields, allowing you to upload the flattened PDF to DocuSign and add the required fields using DocuSign instead.

Please let us know if the issue persists after trying this, and we'll be happy to assist further."

Envelope ID for task 2: "f6c62707-81b1-8107-81e0-ec46f872017a"


**Task 2 response**

"Hi,

We're sorry to hear you're experiencing this issue.

I understand that this template was enabled for Template Matching in your Demo account. However, this setting is account-specific, so it is not automatically carried over when you upload the template to your Production account.

Can you please go to My preferences>> Template matching and make sure that it is enabled from there on your production account. 

After this, please click the three dots next to the template in your Production account and enable Template Matching? This should make the template available for template matching.

For more information about how Template Matching works, please refer to the following support article:
https://support.docusign.com/s/document-item?language=en_US&bundleId=jux1643235969954&topicId=qsw1578456612287.html&_LANG=enus

If you've already enabled Template Matching in your Production account and are still experiencing the issue, please let us know, and we'll be happy to investigate further."


#**In Task 4:**

Error message 1: "{
  "errorCode": "INVALID_REQUEST_PARAMETER",
  "message": "The request contained at least one invalid parameter. Invalid value for xPosition, must be greater than or equal to 0."
}

Fixed by this: Fixed xPosition to a positive value, 


Error message 2: "{
  "errorCode": "ENVELOPE_HAS_DUPLICATE_RECIPIENTS",
  "message": "The specified envelope has duplicate recipients."
}"

Fixed by: recipientId is now "1" and "2"  (Unique ids)


Error message 3: "{
  "errorCode": "TAB_REFERS_TO_MISSING_DOCUMENT",
  "message": "The DocumentId specified in the tab element does not refer to a document in this envelope. Tab refers to DocumentId 2 which is not present."
}"

 Fixed to "1" since only one document exists in the envelope,


 Error message 4: "{
  "errorCode": "TAB_PAGENUMBER_IS_NOT_IN_DOCUMENT",
  "message": "The pagenumber specified in the tab element is not in the document that the tab refers to. Tab on Page 2 of Document 1 for Recipient 2"
}"

Fixed to 1 as the document has only 1 page,


Error message 5: "{
  "errorCode": "INVALID_EMAIL_ADDRESS_FOR_RECIPIENT",
  "message": "The email address for the recipient is invalid. The recipient Id follows. Recipient Id: 2"
}
"

Fixed by adding a valid email for Bruce Wayne, 


Error message 6: " {
  "errorCode": "ENVELOPE_IS_INCOMPLETE",
  "message": "The Envelope is not Complete. A Complete Envelope Requires Documents, Recipients, Tabs, and a Subject Line."
}"

Fixed by adding "emailSubject": "Please sign this document"

