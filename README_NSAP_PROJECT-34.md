# 🧠 Predicting Eligibility for NSAP Schemes using Machine Learning

This project was developed as part of the **IBM SkillsBuild for Academia** Capstone — Machine Learning Problem Statement 34.

## 🏁 Problem Statement

The **National Social Assistance Programme (NSAP)** is a social welfare scheme by the Government of India, aimed at providing financial assistance to:
- Elderly citizens
- Widows
- Persons with disabilities

Each sub-scheme under NSAP has distinct eligibility criteria. Manual verification and allocation of schemes is time-consuming and error-prone. This project builds a **machine learning model** that predicts the **most appropriate NSAP scheme** based on an applicant's demographic and socio-economic data.

---

## 🎯 Project Objective

> To design, build, and deploy a multi-class classification model to automatically predict which NSAP sub-scheme an individual is eligible for, using district-wise socio-economic data.

---

## 🗃️ Dataset

- **Source**: [AI-KOSH Open Data Platform](https://aikosh.indiaai.gov.in/)
- **Dataset**: [District-wise Pension Data under NSAP](https://aikosh.indiaai.gov.in/web/datasets/details/district_wise_pension_data_under_the_national_social_assistance_programme_nsap_1.html)

- **Features include**:
  - Total male/female/transgender beneficiaries
  - Social group breakdown (SC/ST/OBC/GEN)
  - Aadhaar and mobile availability
  - Target label: `schemecode` (IGNOAPS, IGNWPS, IGNDPS)

---

## 🧪 Tools & Technologies Used

- **Platform**: IBM Cloud Lite
- **ML Studio**: IBM Watsonx.ai Studio
- **AutoML Engine**: IBM AutoAI
- **Programming**: Python (for preprocessing, optional)
- **Deployment**: Watsonx.ai Runtime, Deployment Space, REST API

---

## ⚙️ Step-by-Step Workflow

### 🔹 Step 1: IBM Cloud Setup
1. Visited [IBM Cloud](https://cloud.ibm.com/)
2. Cleared existing resources via the Resource List.
3. Created a Watsonx.ai Studio instance (Free Lite plan).

### 🔹 Step 2: Project and AutoAI Creation
1. Launched Watsonx.ai Studio.
2. Created a new project with cloud object storage.
3. Associated the Watsonx.ai Runtime service.
4. Clicked on “Build a Machine Learning Model Automatically (AutoAI)”.
5. Uploaded the AI-KOSH dataset.
6. Selected `schemecode` as the prediction target.

### 🔹 Step 3: Model Training
- AutoAI generated **9 model pipelines**.
- **Pipeline 9 (Batched Tree Ensemble Classifier)** achieved **100% accuracy**.
- Reviewed performance using leaderboard, relationship map, and visual summaries.

### 🔹 Step 4: Deployment
1. Promoted the best model to a Deployment Space.
2. Created a new deployment using Watsonx.ai Runtime.
3. Tested predictions with custom random values.

---

## 📸 Screenshots

> The following screenshots are embedded in the [Project Presentation PDF](#) and demonstrate the full project lifecycle:

- Project Initialization in IBM Watsonx.ai Studio  
- Workflow: Data Processing to Model Selection  
- Feature Relationship Map  
- Completed Progress map Model
- Model Comparison & Performance Leaderboard 
- Testing Interface for Prediction 
- Prediction Output Table

*(See `project_presentation.pdf` in this repo)*

---

## 📊 Results

| Metric         | Value     |
|----------------|-----------|
| Accuracy       | 100%      |
| Top Model      | Pipeline 9 (Batched Tree Ensemble Classifier) |
| Prediction Targets | IGNOAPS, IGNWPS, IGNDPS |
| Confidence     | 97–100% for test records |

---

## ✅ Conclusion

This project successfully demonstrated that machine learning can be applied to automate scheme eligibility under the NSAP program. The model trained and deployed on IBM Cloud can be integrated into government systems to reduce manual effort and improve accuracy in scheme allocation.

---

## 🚀 Future Scope

- Integrate with real-time applicant data.
- Add support for more NSAP schemes.
- Use Explainable AI tools (SHAP/LIME) to enhance transparency.
- Implement continuous model learning with feedback.

---

## 📚 References

- [AI-KOSH NSAP Dataset](https://aikosh.indiaai.gov.in/)
- [IBM Cloud Docs](https://cloud.ibm.com/docs)
- [NSAP Scheme Guidelines](https://nsap.nic.in/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- IBM SkillsBuild for Academia – Problem Statement 34

---

## 📄 License

This project is for educational and demonstration purposes as part of the IBM SkillsBuild for Academia ML Capstone. All dataset sources are publicly available under open government data licensing.

---

## 👤 Author

**SUPRIT AKKI**  
[Jain College of Engineering & Technology] – [CSE]  
Project for IBM SkillsBuild Capstone (2025)
