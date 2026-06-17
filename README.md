# Static Website Hosting on AWS S3

## Project Overview
A static landing page deployed and hosted on Amazon S3 using the static website hosting feature. This is my first hands-on cloud project as part of my cloud security and architecture learning journey.

---

## Architecture
```
Browser → AWS S3 Bucket (Static Website Hosting Enabled)
```

---

## Services Used
- **Amazon S3** — object storage and static website hosting
- **IAM** — bucket policy for public read access
- **AWS Console** — manual deployment

---

## What I Did
1. Created an S3 bucket with a unique name
2. Uploaded `index.html` and `styles.css`
3. Enabled static website hosting and set index document
4. Disabled "Block all public access"
5. Added a bucket policy to allow public read on all objects
6. Accessed the live site via the S3 website endpoint URL

---

## Key Concepts Learned
- How S3 static website hosting differs from regular object URLs
- How bucket policies control public vs private access
- The role of IAM in controlling who can do what in AWS
- Why blocking public access is the default (security best practice)

---

## Security Observations
- Public access should only be opened intentionally and for a known reason
- For production, this should sit behind CloudFront with HTTPS
- Bucket versioning should be enabled to recover from accidental deletions
- Server access logging should be turned on for visibility

---

## Live URL
> http://badaki.s3-website.eu-north-1.amazonaws.com

---



## Next Steps
- [ ] Add CloudFront for HTTPS and CDN
- [ ] Enable S3 versioning
- [ ] Enable server access logging
- [ ] Deploy an EC2 instance and host a dynamic version
