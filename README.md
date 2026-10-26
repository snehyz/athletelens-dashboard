# AthleteLens dashboard prototype

Responsive website prototype for **AI-Driven Multidimensional Athlete Performance Assessment and Clinical Decision Support System**.

## What it does
- Shows a dashboard overview based on project details: 150 football athlete records, 37 columns, XGBoost regression metrics.
- Opens an assessment form for athlete demographics and selected physical, technical, and match criteria described in the report (age, gender, position, height, weight, sprint timings, Yo-Yo score, passing accuracy, assists, shots, shooting, tackling, crossing).
- Displays a demo performance index and suggests three focus areas based on the entered indicators.
- Marks injury-risk assessment as planned, not implemented.

## Important limitations
The assessment form does **not** yet submit to your actual database or trained XGBoost model. The displayed index is a transparent illustrative calculation and must not be represented as a genuine model prediction. The focus suggestions are general demo suggestions. The report describes 37 dataset columns but does not provide their complete exact names in the text; match every input to your actual dataset's column names and required preprocessing before connecting the model. Injury risk requires a separate validated model and suitable labels.

## Preview
Open `index.html` in a browser.

## Deploy to Vercel
1. Create a GitHub repository and upload `index.html` (and this README).
2. In Vercel, choose **Add New → Project** and import the repository.
3. Select **Other** if asked for a framework; leave build command and output directory empty/default for this static page.
4. Deploy.

To produce genuine predictions, create a server-side API that loads your saved model and applies the same feature order and preprocessing used during training. The browser should send the entered values to that API and display its response. Do not put database credentials or model secrets in client-side code.
