# Epochlock

A [free](https://en.wikipedia.org/wiki/Free_software) and [open-source](https://en.wikipedia.org/wiki/Open-source_software) ([FOSS](https://en.wikipedia.org/wiki/Free_and_open-source_software)), secure, [self-hostable](https://en.wikipedia.org/wiki/Self-hosting_(web_services)) and [cross-platform](https://en.wikipedia.org/wiki/Cross-platform_software) application for creating, managing, and sharing time capsules.

A **time capsule** holds some data, called **content**, that was **encapsulated** by the **initiator**, and it will be **released** to its **recipients** on a particular **liberation** date.

## Value proposition

Epochlock will be a solution for preserving memories or sensitive data, sending messages to the future and securely storing and sharing personal information.

For users who value complete control over their data, Epochlock will offer a self-hosting option. This allows users to host the application on their own servers or cloud platforms, ensuring that their data remains within their personal infrastructure. Self-hosting, alongside open-source, empowers users with greater control, privacy, and the ability to customize the application according to their specific requirements.

Epochlock will be designed to be cross-platform, supporting a wide range of devices and operating systems. Whether users prefer to access the application from their desktop, mobile devices, or web browsers, Epochlock ensures a consistent experience across platforms, enabling seamless access to time capsules from anywhere, at any time.

Epochlock aims to be the ideal choice for individuals and organizations seeking a reliable and versatile time capsule application.

### Use cases

Practical examples of use cases for this application:

* **Time-locked Announcements**: Epochlock could be used to send time-locked announcements or messages to a group of recipients. For example, a company may use Epochlock to schedule the release of important announcements or updates to employees or customers on a specific date in the future. This could be useful for event organizers, businesses, or community groups planning future events or promotions.
* **Secure Storage and Sharing**: Epochlock provides a secure platform for storing and sharing sensitive information. Users could encrypt the content of their time capsules, ensuring that only authorized recipients with the password could access the information.
* **Inheritance Planning**: Users could utilize Epochlock to securely store and share sensitive information, such as wills, estate plans, or passwords, with designated recipients at a future date or after their passing (using a Continuous Countdown time capsule). This ensures that important information is safely transmitted to the intended recipients when the time is right. This could be an interesting solution in regards to transferring crypto currencies wallets private keys for example.
* **Creative Projects**: Epochlock could be a valuable tool for artists, writers, musicians or other creators who want to experiment with time-based projects. They could use the application to release their work gradually over a specific timeline, building anticipation and engaging their audience in a unique way.
* **Messages to Future / Reminders**: Epochlock will allows users to send messages to themselves or others in order to create reminders through time capsules. They could reflect, set goals, and schedule the release of capsules for self-reflection, motivation, and staying organized.
* **Dead man's switch**: Continuous Countdown time capsule enables a captive person to leverage a ["dead man's switch"](https://en.wikipedia.org/wiki/Dead_man%27s_switch) concept, ensuring that if they fail to reset the countdown within a specified time period, the capsule automatically releases their message to the predefined recipients. This mechanism empowers the captive person, providing a sense of security and the ability to expose injustices, provide evidence, or shed light on hidden truths. It serves as a tangible means of fighting against captivity, leaving a lasting impact on the world and potentially prompting action, even in dire circumstances.

## Name

The name "Epochlock" is composed of the two words "epoch" and "lock".

"Epoch" denotes a specific instant in time. It also has a [computer science meaning](https://en.wikipedia.org/wiki/Epoch_(computing)): a date and time from which a computer measures system time. It's a reference to the [Unix Epoch](https://en.wikipedia.org/wiki/Unix_time).

The second word "lock" refers to the idea that the content of the capsule is not accessible by the recipients until the time has come. It also denotes the fact that the content can be encrypted to ensure that it is securely stored and that no one can read it, except for the initiator and the recipient(s) that know the password.

## Requirements

### Functional requirements

* User account registration + login process for users to issue and manage their time capsules.
* Ability to send time capsules through various channels such as emails, shareable links, capsule identification code (**CID**), ... A capsule link will lead to a page in the application where the recipients can see the type of the capsule and how much time is left before the liberation. Recipients are free to **subscribe** to a capsule (using the link or the CID) in order to have easy access to it on the application.
* Password protected content encryption (opt-out [E2EE](https://en.wikipedia.org/wiki/End-to-end_encryption)) to ensure the confidentiality of the capsule.
* Support for different types of capsules:
  * **Immediate**: the capsule is released as soon as the initiator creates it
  * **Scheduled**: the initiator fixes a specific date when the capsule will be released (if not cancelled by sender before the date)
  * **Continuous Countdown**: the initiator defines a maximum time period when creating the capsule. They can reset the countdown to its initial value at any moment. The capsule will be release if the initiator doesn't prevent the liberation before the countdown runs out.
* Alerts and notifications subscription to inform recipients and initiators about the state of a time capsule.
* Cross-platform compatibility will allow users to access and interact with their time capsules from various devices.

### Technical specifications

#### Client

* Developed using the [Dart](https://dart.dev/) programming language, powered by the [Flutter](https://flutter.dev/) framework for cross-platform compatibility and high level object-oriented programming.
* Intuitive and easy to use design for the user interface.
* Implementation of End-to-End content encryption as well as [HTTPS](https://en.wikipedia.org/wiki/HTTPS) support to ensure secure client-server communication and storage of the time capsules.

#### Server

* Developed using the [Rust](https://www.rust-lang.org/) programming language.
* Packaged and distributed using [Docker](https://www.docker.com/) for easy self-hosting capabilities.
* Official project instance hosted on a [Virtual Private Server](https://en.wikipedia.org/wiki/Virtual_private_server) with its own domain for easy accessibility.
* Automated backup and recovery mechanisms to prevent data loss and ensure the availability of time capsules even in the event of server failures or other technical issues.

### Constraints

* **Budget constraints**: The project must be cost-effective, considering expenses such as domain registration and server hosting.
* **Time constraint**: The first major release must be completed before the end of the autumn semester 2023.
* **Legal considerations**: Users must be explicitly informed that the server provider is not responsible for the storage or delivery of their data, and no warranties are provided. Additionally, the option for self-hosting will be available if users wants more control over their data or server performances.

### Deliverables

Project:

* Front-End client application with a user-friendly, easy to use interface.
* Back-end server application for handling capsule storage and liberation.
* Comprehensive application documentation that includes installation instructions, user guides, and developer documentation to assist users in setting up and using Epochlock. This documentation should be regularly updated to reflect any changes or new features.

Academic:

* Report / Document explaining the technology and procedures used in the development of Epochlock.
* Weekly changelogs, progress reports documentation as well as a weekly meeting with project supervisor.
* Oral presentation to showcase the features and capabilities of Epochlock and retrospect on the project execution.

## Future ideas

What follows are some ideas of further improvements that could be added to the app after the first release:

* **Media support**: Users could create time capsules to preserve their personal memories, such as photos or videos.
* **Collaborative content**: Epochlock could support collaborative time capsules, where multiple users contribute content to a shared capsule.
* **Social media integration**: time capsules could be released directly through a social media post.
* **[2FA](https://en.wikipedia.org/wiki/Multi-factor_authentication)**: The application could also utilize two-factor authentication for enhanced security regarding user accounts and capsule content access.
* **Dynamic message content**: the content of the capsule could change over time, till the liberation date. This could be useful to provide additional information at the liberation time, like localization of the initiator on liberation for example.
