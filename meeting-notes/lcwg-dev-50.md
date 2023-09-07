# Light Client Working Group Devs Meeting 50
### Meeting Date/Time: Thursday, May 18th, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Lux (Zingo), Mandeep (Nighthawk), John (ZF), Matt (Nighthawk), Adi (Nighthawk)
### Notes: Adi

# 1. General Notes
 * SDK upgrade review for Android 14:
   - During the SDK upgrade review, an issue was identified with the Gradle toolchain autoprovisioning API.
   - Specifically, there is a lack of JDKs 1.8 available for Mac M1 devices, as noted in the link: https://adoptium.net/temurin/releases/?version=8
   - A possible workaround to address this issue is to set the minimal toolchain to version 11.
   - However, for a proper and more comprehensive solution, it is recommended to upgrade the wizards to Gradle version 7.6.
   - Additionally, adding the https://github.com/gradle/foojay-toolchains plugin into the settings plugins would also be beneficial.


### Expanded using ChatGPT May 24 Version