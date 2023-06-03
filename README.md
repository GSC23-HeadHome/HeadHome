<br>
<div align="center">
    <div >
        <img width="200px" src="https://firebasestorage.googleapis.com/v0/b/gsc23-12e94.appspot.com/o/members%2Fheadhome_square.png?alt=media&token=96a55b42-7c9f-4e68-b41f-d986efe79c01" alt=""/>
    </div>
    <div>
            <h3><b>HeadHome</b></h3>
            <p><i>Your companion, every step of the way</i></p>
    </div>      
</div>
<br>
<h1 align="center">HeadHome</h1>

![HeadHome](assets/headhome.png)

**HeadHome: Your Go-To Dementia Aid Solution**

HeadHome aims to reduce the dangers posed by dementia wandering, and provide the caregivers of our dementia counterparts with an effective means of locating them and safely returning them home.

## Problem Statement

<br/>
<blockquote align='center'>
<h3>“6 in 10 people with dementia will experience wandering episodes.”

\- Alzheimer's Association

</h3>
</blockquote>
<br/>

With the onset of an ageing population, the prevalence of dementia has risen drastically over the years. People with dementia often **experience confusion, disorientation, and memory loss**, which can cause them to wander away from their homes or care facilities without realising where they are going. Dementia wandering episodes are not only **physically dangerous** for patients, but also **emotionally traumatic** for their caregivers.

## 🎥 &nbsp;Demo Video

<a href="https://www.youtube.com/watch?v=LzYhsY_ZCrk&ab_channel=JingXuanOng"><img src="./assets/demo-video-thumbnail.png" /></a>

> Video Link: https://www.youtube.com/watch?v=LzYhsY_ZCrk&ab_channel=JingXuanOng

## 🛠️ &nbsp;Key Functionalities

![Key Functionalities](assets/key-functionalities.jpg)

### 1. Dementia Patient

The **`Dementia Patient`** can request for help from their **`Caregiver`** and begin the navigation back home by tapping on the red **`Navigate Home`** button on their home page. The application will also begin navigation when the **`Patient`** leaves the configurable safezone radius around their home, or when they press the red button the companion wrist wearable device.

This will display a route home on the Google Maps widget. This route will be updated as the patient goes along, rerouting when necessary.

The patient would each have an Authentication ID which is used to ensure that the **`Volunteer`** will only have access to the **`Patient's`** home address when they have actually met them.

### 2. Caregiver

The **`Caregiver`** will receive a notification when their respective **`Patients`** have started to navigate home. This will inform them about the **`Patient's`** current location, and also allow them to choose to send an SOS alert signal to **`Volunteers`**.

The **`Caregiver`** will then be able to contact the **`Volunteers`** who have started to guide the **`Patient`** back home through the **`contact`** button of the application.

### 3. Volunteers

**`Volunteers`** would be able to view all nearby SOS alerts, and select the **`Patient`** they wish to help. The app would provide them with the current location of the **`Patient`**, and also allow them to redirect to Google Maps to find their way to these **`Caregivers`**.

Thereafter, when the **`Volunteers`** reach the **`Patient`**, they would be able to start leading them home after verifying the `Patient's` Authentication ID

<a href="https://raw.githubusercontent.com/GSC23-HeadHome/HeadHome/main/assets/user-flow-diagram.png">
<img src="./assets/user-flow-diagram.png" />
</a>

> Click image to enlarge.

This user flow diagram gives an overview of the communication flows between the various stakeholders through HeadHome.

## 🎯 &nbsp;UN's Sustainable Development Goals & Targets

### SDG 3: Good Health and Well-Being (Target: 3.6)

![SDG3](assets/SDG3.png)

HeadHome directly addresses the issue of **dementia wandering**.

Wandering episodes can bring danger to patients such as traffic incidents, with no way to contact their caregivers. Thus, caregivers might feel the need to micromanage their patients, causing significant caregiver stress.

HeadHome can help these patients by providing clear and simple instructions on the wearable to guide the patient home. It also sends alerts to their caregiver whenever they need help, removing the need for constant tracking and monitoring.

### SDG 11: Sustainable Cities and Communities (Target: 11.a.1)

![SDG11](assets/SDG11.png)

HeadHome **leverages the power of the community** to improve the lives of dementia patients. Most caregivers have full-time jobs and cannot be with their loved ones 24/7. To ensure that dementia patients can receive help anytime, we will recruit registered volunteers in the community. Caregivers can send out an SOS message to volunteers near the vulnerable patient, who can guide the patients back home. This builds up an inclusive and socially aware community, which can help these patients when they are in need.

## 👨🏻‍💻 &nbsp;Technology Stack

<div align="center">
<kbd>
<img src="./assets/icons/Flutter.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Dart.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Firebase.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Go.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Gin.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/GCP.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Maps.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/Arduino.png" height="60" />
</kbd>
<kbd>
<img src="./assets/icons/ESP32.png" height="60" />
</kbd>
</div>
<div align="center">
<h4>Flutter | Dart | Firebase | Go | Gin | Google Cloud Platform | Google Maps Platform | Arduino | ESP32</h4>
</div>

## ☁️ &nbsp;Enterprise Cloud Architecture & Services

<a href="https://raw.githubusercontent.com/GSC23-HeadHome/HeadHome/main/assets/cloud-architecture.png">
<img src="./assets/cloud-architecture.png" />
</a>

> Click image to enlarge.

### 1. Presentation Layer

**Users** of HeadHome will directly interact with the Presentation Layer, namely the HeadHome wearable built with **Arduino & ESP32**, as well as the HeadHome mobile application built with **Flutter & Dart**. Any business or computational logic is abstracted onto the serverless backend hosted on **Cloud Run**. With Cloud Run's auto-scaling and load balancing capabilities, in the event of more traffic, our backend is able to seamlessly scale horizontally to meet the growing demands of the application. Due to the flexibility and versatility of Cloud Run, an external load balancer in the form of Google's **Cloud Load Balancing** could be tapped on to deploy our backend to multiple regions and further reduce latencies and downtime.

**For more information:**

HeadHome hardware wearable: [Link](https://github.com/GSC23-HeadHome/HeadHome-Hardware)

HeadHome frontend mobile application: [Link](https://github.com/GSC23-HeadHome/HeadHome-App)

HeadHome backend: [Link](https://github.com/GSC23-HeadHome/HeadHome-Backend)

### 2. CI/CD Pipeline

For **developers**, the HeadHome project comes with a fully integrated CI/CD pipeline equipped with auto-deployment from **Github**. Any code changes to the [HeadHome Backend Repository](https://github.com/GSC23-HeadHome/HeadHome-Backend) will be automatically mirrored onto **Google Cloud Source Repositories** and containerised to **Artifact Registry** via **Cloud Build**. Coupled with **Secret Manager**, the backend container is deployed serverless via **Cloud Run**.

### 3. Backend Services & Storage Layer

Many miscellaneous backend and storage services abstracted and handled via **Google Cloud**, as detailed below.

| Google Cloud Service     | Purpose & Use                                                                                 |
| ------------------------ | --------------------------------------------------------------------------------------------- |
| Google Maps Platform     | Directions API to display route back home & Maps SDK to display map on the mobile application |
| Firebase Cloud Messaging | Handles push notifications to caregivers                                                      |
| Firebase Authentication  | Handles all authentication related painpoints                                                 |
| Firebase Storage         | Stores profile assets for the frontend application                                            |
| Firebase Cloud Firestore | Main production database for all business storage purposes                                    |

### 4. Analysis Layer

![looker dashboard](./assets/looker-dashboard.png)

For **business stakeholders** who are looking to gather critical business intelligence, such as the amount of resources required for each geographical area, the data from our **Cloud Firestore** database is streamed to **Google BigQuery**, and pumped to **Looker Studio** as a business intelligence monitoring platform.

### 5. Operations Layer

![cloud monitoring dashboard](./assets/cloud-monitoring-dashboard.png)

For **business stakeholders** looking to gather operational metrics, HeadHome comes with an Operations Layer including **Cloud Monitoring** and **Cloud Logging**. These Google Cloud Platform services are integral to gain a more holistic profiling of our users and a better understanding of our services internally via uptime checks and alerts.

# Getting Started

[Flutter `(Version 2.19.2+)`](https://docs.flutter.dev/get-started/install) must be installed to run this application.

Detailed instructions on how to run the application can be found [here](https://github.com/GSC23-HeadHome/HeadHome-App/blob/main/README.md#getting-started).

## 👥 &nbsp;Contributors

| <a href="https://github.com/chayhuixiang"><img width="180px" src="https://firebasestorage.googleapis.com/v0/b/gsc23-12e94.appspot.com/o/members%2Fhuixiang.jpeg?alt=media&token=96a55b42-7c9f-4e68-b41f-d986efe79c01" alt=""/></a> | <a href="https://github.com/changdaozheng"><img width="180px" src="https://firebasestorage.googleapis.com/v0/b/gsc23-12e94.appspot.com/o/members%2Fdaozheng.jpeg?alt=media&token=96a55b42-7c9f-4e68-b41f-d986efe79c01" alt=""/></a> | <a href="https://github.com/Trigon25"><img width="180px" src="https://firebasestorage.googleapis.com/v0/b/gsc23-12e94.appspot.com/o/members%2Fmarc.jpeg?alt=media&token=96a55b42-7c9f-4e68-b41f-d986efe79c01" alt=""/></a> | <a href="https://github.com/ongjx16"><img width="180px" src="https://firebasestorage.googleapis.com/v0/b/gsc23-12e94.appspot.com/o/members%2Fjingxuan.jpeg?alt=media&token=96a55b42-7c9f-4e68-b41f-d986efe79c01" alt=""/></a> |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <div align="center"><h3><b><a href="https://github.com/chayhuixiang">Chay Hui Xiang</a></b></h3><p><i>Nanyang Technological University</i></p></div>                                                                               | <div align="center"><h3><b><a href="https://github.com/changdaozheng">Chang Dao Zheng</a></b></h3></a><p><i>Nanyang Technological University</i></p></div>                                                                          | <div align="center"><h3><b><a href="https://github.com/Trigon25">Marc Chern Di Yong</a></b></h3></a><p><i>Nanyang Technological University</i></p></div></a>                                                               | <div align="center"><h3><b><a href="https://github.com/ongjx16">Ong Jing Xuan</a></b></h3></a><p><i>Nanyang Technological University</i></p></div>                                                                            |
