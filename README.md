# Blog_5

What is CloudWatch AWS service and how can it be used in trigerring your Lambda function?

Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides you with data and actionable insights to monitor the AWS services that you are using. However my focus here is specifically on trigerring Lambda not any other service in AWS.

I will make it as simple as possible, Once you go to the Cloudwatch page, and you create a new event, you will have to choose which AWS service you want to monitor, here we will choose Lambda, then you specify the Lambda function name you want to trigger. after that it sends you to a new page where you specify the "Cronjob" or basically the timing for when you want to trigger your Lambda function.

Cronjob has six different elements and each one refers to a differnt time, The example below exaplains exaclty how you can build your Cronjob and each of the elements stands for.

Minutes|Hours|Day of month|Month|Day of week|Year|(Meaning)

0      | 10  |    *       |  *  |    ?      | *  |(Run at 10:00 am (UTC) every day)

15     | 12  |    *       |  *  |    ?      | *  |(Run at 12:15 pm (UTC) every day)

0      | 18  |    ?       |  *  |  MON-FRI  | *  |(Run at 6:00 pm (UTC) every Monday through Friday)

0      |  8  |    1       |  *  |    ?      | *  |(Run at 8:00 am (UTC) every 1st day of the month)

0/15   |  *  |    *       |  *  |    ?      | *  |(Run every 15 minutes)

0/10   |  *  |    ?       |  *  |  MON-FRI  | *  |(Run every 10 minutes Monday through Friday)

0/5    |8-17 |    ?       |  *  |MON-FRI    | *  |(Run every 5 minutes Monday through Friday between 8:00am and 5:55pm(UTC)) 
