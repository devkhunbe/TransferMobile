# Transfer-Mobile

# MU


# Source-code

```
seatin-hita/mu_app_mobile
branch: main
```

### GIT REPO-config

```https://github.com/devbay225/game-profile/blob/main/mu/release/config.json```

 - Note: You should create api config, instead using this link.

## System require

Install Node module

Install React-native 

Install Android studio [lastest version]

Install Xcode [lastest version]

Install CocosCreator v2.1.3


## Distribute with CodePush

- [What is CodePush](``https://microsoft.github.io/code-push/`)

### Create account and login CODEPUSH

[**https://appcenter.ms/**](https://appcenter.ms/)

Login with Google darasa account - open project

Open screen **Distribute ⇒ codePush** 


### Access Key

Open screen Distribute ⇒ codepush, click to icon setting on the right screen

Key prod 

```jsx
Za5aPeebuOmwlIrVCIa8xy1Lpw4B6lTHSdAzF
```

Key stg

```jsx
X2e01DJR3FDIpvTHPhkQu_-5bqhL6XWtWWhYz
```

### How to use Access key

**Android project**

- Add key to string file:
`android/app/src/main/res/values/strings.xml`

```xml
<resources>
    <string moduleConfig="true" name="CodePushDeploymentKey">[KEY]</string>
</resources>
```

**IOS Project** 

- Add key to Plist file
    
    `ios/MuApp/Info.plist`
    

```xml
<key>CodePushDeploymentKey</key>
	<string>[Key]</string>
```

### Build and deploy

- **Install AppCenter-CLI in terminal**
    - `npm install -g appcenter-cli`
    - Login with account code
 
- Deploy STG
    - Run file codepush.sh : `bash codepush.sh stg android`
- Deploy prod
    - Run file codepush.sh : `bash codepush.sh prod android`

**How to update app?**

After execute bash file. CodePush will push file Bundle to AppCenter.  When user open application.  App will be detect  if different ***version*** then show popup update application.

Version is auto increase but we need follow a rule:

Your target-binary-version "2.1" will be treated as "2.1.X".

**Note:**
- If application not show update poup, You need to turn on require update on Dashboard :https://appcenter.ms/users/bay-hikotech.io/apps/MU/distribute/code-push/Production/v30
- [Example](https://blog.effectussoftware.com/wp-content/uploads/2021/05/img-codepush-1024x560.png)

## Disribute store

- IOS: [APP](https://apps.apple.com/kh/app/broasted/id1641874985)
  - Contact with partner to distribute app. username_tele: xxx (!STOP) -(no support more)
- Android [APP](https:mu9.casino.page.link/app)

## Firebase Dynamic Link
 - https://console.firebase.google.com/project/muapp-60776/durablelinks/links/https:~2F~2Fmu9casino.page.link
**NOTE:** When update domain website, We need to update Dynamic Link
- How add new custom prefix : [READ MORE](https://support.google.com/firebase/answer/9021429)
