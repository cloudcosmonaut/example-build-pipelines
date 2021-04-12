# Example Xamarin Build pipelines

Some examples to create build pipelines for your Xamarin apps. These contain two stages; one for Acceptance and one for Production.

## iOS

Prerequisite: 
- Access to [Apple Developer Program](https://developer.apple.com/programs/)
- Pre set-up App in [AppStore Connect](https://developer.apple.com/programs/)
- [Provisionting Profiles](https://developer.apple.com/account/resources/profiles/list)
- [Distribution Certificate](https://developer.apple.com/account/resources/certificates/list) with private key
- [Set-up Sevice Connection](https://docs.microsoft.com/en-us/appcenter/distribution/stores/apple)


### Templates
- [Azure DevOps](azure-ios-release.yml)

To use this template, you need to set-up the following:
- Add mobile provisioning profiles to soure repository
- Add private key (p12) to [Secure files section in Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/secure-files?view=azure-devops)
- Add password of your private key to a secure value in the pipeline
- Update the App Identifier, Team Id, Signing Identity, Signing Profile Id in the YML file for both environments

## Android

Prerequisite: 
- [Google Play Developer account](https://developer.android.com/)
- Pre set-up App in [Google Play Console](https://play.google.com/console/)
- [Set-up service connection to Google Play](https://docs.microsoft.com/en-us/appcenter/distribution/stores/googleplay).
- Keystore containg with key alias for signing the Android App

### Templates
- [Azure DevOps](azure-android-release.yml)

To use this template, you need to set-up the following:
- Add mobile provisioning profiles to soure repository
- Add private key (keystore) to [Secure files section in Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/secure-files?view=azure-devops)
- Add the password of your keystore and alias to a secure value in the pipeline
- Update the Keystore alias, and references to secure values from your pipeline

