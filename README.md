# Replication Using S3 in AWS Cloud
The following is an illustration on how I replicated a static web page to different availability zones using S3 on Amazon Web Services. Using S3 replication allows for easier bucket management in that buckets will automatically be synchronized for us. Another reason would be to have content more closely available to clients in another region. In this example I'll be replicating my [previously made](http://github.com/hann-cyber/AWS-S3-StaticWeb) static webpage, which is being hosted in the US East (Ohio) region to another convenient location.

1. To begin the process I first make another bucket. However, notice my repdemo-destination is hosted in Paris, Europe.

<p align="center">
 <img src="https://i.imgur.com/1Y5pIaz.png">
</p>

2. Now, I'll create a replication rule.

<p align="center">
 <img src="https://i.imgur.com/6OsRFG3.png">
</p>

Configuring:

To keep it simple, I'll just name it "RepRuleDemo", but an important feature is to "Apply to all objects in the bucket" under "Source bucket" options. This will enable replication to all uploaded files in a bucket to another.

<p align="center">
 <img src="https://i.imgur.com/PmqVLPU.png">
</p>

Confirm the replication rule is "Enabled".

<p align="center">
 <img src="https://i.imgur.com/IPi2PSd.png">
</p>

When navigating to my destination bucket, again, located in Paris we can confirm the exact same files from the previous project have been copied over. Now, I have my resources more conveniently available to clients around Europe.

<p align="center">
 <img src="https://i.imgur.com/bg16utN.png">
</p>
