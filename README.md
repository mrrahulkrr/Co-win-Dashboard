In this project, I have build a **CoWIN Dashboard** by applying the react concepts I have learned till now.

### Refer to the images below:

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-output.gif" alt="" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

**Failure View**

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-failure-view-output.gif" alt="cowin-dashboard-failure-view-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

## Completion Instructions

<details>
<summary>Functionality added</summary>
<br/>

The app will have the following functionalities

- When the page is opened,
  - An HTTP GET request will be made to **covidVaccinationDataApiUrl**
  - **_loader_** will be displayed while the HTTP request is fetching the data
  - After the data is fetched successfully, the response received will be displayed using different charts from `recharts`
  - The last 7 days vaccination data will be displayed using the `BarChart` component from `recharts`
  - The data for vaccination by gender and vaccination by age will be displayed as two different pie charts using the `PieChart` component from `recharts`
  - If the HTTP GET request made is unsuccessful, then the [FailureView](https://assets.ccbp.in/frontend/react-js/api-failure-view.png) will be displayed

</details>

<details>

<summary>API Requests & Responses</summary>
<br/>

**covidVaccinationDataApiUrl**

## API: `https://apis.ccbp.in/covid-vaccination-data`

#### Method: `GET`

#### Description:

Returns a response containing the list of Products

#### Success Response

```json
{
  "last_7_days_vaccination": [
    {
      "vaccine_date": "30th Jul",
      "dose_1": 3757930,
      "dose_2": 1817805
    },
    ...
  ],
  "vaccination_by_age": [
    {
      "age": "18-44",
      "count": 482792375
    },
    ...
  ],
  "vaccination_by_gender": [
    {
      "count": 4809680,
      "gender": "Male"
    },
    ...
  ]
}
```

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-component-structure-breakdown.png" alt="component-breakdown-structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>
