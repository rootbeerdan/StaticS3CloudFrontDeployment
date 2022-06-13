# :warning: **There are better ways to do this** :warning:

It's much better to use a purpose made tool for this. Below is a (non-exhaustive) list of tools you could use instead (I use Cloudflare Pages):
- Cloudflare Pages
- GitHub Pages
- AWS Amplify
- Azure Static Web Apps

I am keeping this archived repository around for posterity as it was made during a time when there was not many good options for static webpages.

# StaticS3CloudFrontDeployment
GitHub action to deploy repo to S3 and clear cloudfront cache

## Use
You'll need to do a few things beforehand, this can be automated in CloudFormation or not depending on your skill level.

### Create S3 Bucket
Pretty straightforward, name it something useful, keep it private

### Create CloudFront distibution

Configure it the way you want. If you want to save money, remove every region except US/Canada, assuming you live in North America.

### Create IAM role

This is important that you don't just use your regular access keys, to keep up security. Limit it's access to just write access to buckets, and invalidation of CloudFront cache.

### Help

Feel free to submit an issue if you need help.
