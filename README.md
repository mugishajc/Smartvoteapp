# Smart Vote App

An Android voting app that verifies voters before they cast a ballot: each voter is checked against a national population register and confirmed with the phone's fingerprint sensor.

## Features

- Voter registration and login against a population register API.
- Eligibility check before voting.
- Fingerprint authentication through the Android fingerprint API.
- Ballot screen to choose a candidate and submit a vote.

## Stack

- Android (Java), AndroidX, Navigation drawer
- Android FingerprintManager (`FingerprintHandler.java`)
- Retrofit 2 + Gson, Volley
- PHP REST backends for the voting service and the population register

## API calls

| Method | Path | Purpose |
|---|---|---|
| POST | `population/register` | Register a citizen |
| POST | `population/login` | Log in |
| POST | `vote/registration/check` | Check voter eligibility |

Backend URLs are set in `singleton/RESTApiClient.java` and `singleton/RESTCl.java`.

## Running

Open in Android Studio and run on a device with a fingerprint sensor (minSdk 23).
