# Data_view_Bounce
The _Bounce Data View provides information about bounce data of your email activities in SFMC. The Dates and Times in this data view are stored using Central Standard Time.<br>
SELECT
    b.JobID ,
    b.SubscriberID,
    b.SubscriberKey,
    s.EmailAddress,
    b.EventDate,
    b.Domain,
    b.BounceCategoryID,
    b.BounceCategory,
    b.BounceSubcategoryID,
    b.BounceSubcategory,
    b.BounceTypeID,
    b.BounceType,
    b.SMTPBounceReason,
    b.SMTPMessage,
    b.SMTPCode
FROM _Bounce b
LEFT JOIN _Subscribers s ON b.SubscriberKey = s.SubscriberKey
WHERE b.JobID = '3188130'
