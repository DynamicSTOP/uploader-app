# Uploader App

The goal: Have a web page that allows uploading multiple files from the phone to s3
with either Google Android Auth, fingerprints, yubikey or Authenticator app.
The app should allow tagging files and storing them into different categories.
Files should be visible after login, but you can also make temp links or qr codes.
S3 should have following lifecycle rule. After 30 days move file to infrequent class storage.
The app should be coded in typescript, eslint checked and covered by unit and integration tests.
___

## RoadMap:

### 1. AWS CloudFormation stacks

- [ ] AWS S3 stack
  - [x] Delete incomplete uploads
  - [x] delete "temp" files
  - [ ] move to infrequent after 30 days 
- [x] AWS CloudFront stack
- [ ] AWS DynamoDB stack
- [ ] AWS API Gateway stack
- [ ] AWS Lambda stack

___

### 2. Basic Page & Upload

- [ ] Build basic page & lambda
- [ ] Upload page files & lambda
- [ ] Make basic upload
    - [ ] Make multipart upload
    - [ ] Multiple files
    - [ ] Files tagging
    - [ ] Update files tagging during upload
- [ ] Make auth (AWS Cognito?)
    - [ ] Fingerprint
    - [ ] Yubikey
    - [ ] Authenticator app
    - [ ] Google Android (bluetooth)
- [ ] Add Files List page
    - [ ] Paginated list
    - [ ] S3 link to open (CF with cookies?)
    - [ ] S3 link to share
    - [ ] QR code to share

___

### 3. Testing

- [ ] Unit tests
- [ ] Integration tests