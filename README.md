# MERIT-HOSPITAL-MANAGEMENT-REPORT-ANALYSIS

<img width="619" height="347" alt="P1" src="https://github.com/user-attachments/assets/53160897-ab55-4b1d-b33e-07b11c30a445" />

## Problem Statement

It’s the time for the annual report at MERIT hospital, and the management wants to know the patient’s inflow, service usage and the operations of the hospital throughout the year 2025. They seek to know which department (service) is their strength and where they need to invest more in the new year in relation to employing more hands and purchase of more facilities that will make it seamless for their patients to have access to a better healthcare system in the new year. 

## Dataset Overview and Structure
This project captures datasets on patient flow, service utilization and workforce operations. It is composed of four tables interrelated, each representing a key operational domain within the hospital. 

  - Patients Table: This table contains key fields including patient id, age, arrival and departure dates, service accessed, satisfaction ratings, and week of visit.
  
  - Staff Table: The staff table stores information about hospital personnel, including staff id, staff names, professional roles, and associated services. It serves as a           dimension table for workforce analysis.

  - Staff Schedule Table: This table captures weekly staff availability and attendance. It records the presence or absence of staff by role, service, and week, enabling           analysis of staffing levels, attendance rates, and workforce reliability.
  
  - Services Weekly Table: The services weekly table is an aggregated fact table containing weekly operational metrics per service. It includes available beds, patient           requests, admissions, refusals, patient satisfaction scores, staff morale indices, and notable events.

## Data Model Structure

<img width="532" height="311" alt="image" src="https://github.com/user-attachments/assets/ebb68b34-d34a-427c-a9c7-34bfe16fff9a" />

A snowflake-schema-inspired model was implemented. A dedicated calendar table enables time intelligence and trend analysis. Fact tables are connected through shared dimensions such as service and week, ensuring consistent filtering and accurate aggregation across visuals.

## Research Questions

  1.	How do patient arrivals and admissions change over time?
  2.	Are available hospital beds sufficient to handle patient demand?
  3.	Which hospital services face the highest demand pressure?
  4.	Which services record the highest patient refusals, and why?
  5.	How does staff availability and attendance vary across services and months?
  6.	What is the relationship between staff morale and service performance?
  7.	Where do operational or staffing gaps create inefficiencies in hospital service delivery?

## Analytical Techniques

  -	KPI calculations were implemented using DAX measures.
  -	Ratio-based metrics such as admission rate, refusal rate, attendance rate, and bed occupancy were derived.
  -	Conditional formatting was applied to matrices to visually highlight operational risks and performance variations.
  -	Trend analysis was conducted using line charts to identify seasonal and cyclical patterns.

## Visualization Strategy
The report was structured into two analytical pages:
-	Patients
-	Staff and Services

## Key Findings and Insights

### Patient Insights

<img width="619" height="347" alt="P1" src="https://github.com/user-attachments/assets/3ee7536a-3137-486a-b7e5-abf2a843805c" />

- MERIT hospital received a total of 1000 patients whose average age is 45 and they stayed for an average length of 7 days with 261 in emergency, 250 in surgery, 239 in General Medicine, 236 in ICU and 14 untagged. A deeper drill into the blank service showed a possibility of registration errors as many of the patients have discharge dates of January 2026.
  
- Patients’ arrival showed was highest on Saturdays (154) followed by Wednesday (149) and Friday (148) and September (94) received the highest number of patients in the year.
   
- A 93% bed occupancy rate indicates that the hospital available bed spaces are heavily occupied at every given time leaving them with just 7% of beds free resulting in a decrease in admission strength.
   
- An overall satisfaction rate of 80 further showed that about 39% of the patients are averagely satisfied, 35% highly satisfied, and 25% not satisfied with the service they received.

### Staff and Services Insights

<img width="617" height="344" alt="P2" src="https://github.com/user-attachments/assets/d6829148-e311-4f0e-aab7-5f7688ce33b4" />

- MERIT hospital received a total of 13493 admission requests across services but was only able to admit 5851 patients because they had only 6312 available beds.
  
- The hospital has only 126 staff consisting of 73 nurses, 31 nursing assistants, and 22 doctors with 39 of these staff in emergency, the department that received the highest admission request of 6193, but rejected a whooping 5008 patients, indicating the need to employ more hands and provide more capacity to admit more patients.
   
- A deeper dive into the events of the rejection, a total of 3388 patients were rejected with no reason attached, which could be a result of lack of admission capacity while some others were rejected because of lack of donation, flu, and strike.
  
- The ICU department has 34 staff, received 789 requests, admitted 648 and rejected only 141. The General Medicine department has 28 staff, received 4270 admission requests, admitted 2332 and rejected 1938. The Surgery department received a total of 2241 admission requests, rejected 555 and admitted 1686 patients.
  
- The morale of staff across services (departments) ranged from 71 to 74, which falls within a moderate band, indicating a need to implement targeted staff engagement and workload management strategies to prevent morale decline, particularly in services experiencing high patient demand and operational pressure.
  
- A 60% attendance rate further showed that March (44%), June (46%), and September (44%) had the lowest attendance rate.

## Recommendations
1.	Increase the hospital capacity and staffing by expanding bed availability and recruiting additional staff in high-demand departments to reduce patient rejections and ensure adequate coverage during peak periods.
2.	Increase the hospital capacity and staffing by expanding bed availability and recruiting additional staff in high-demand departments to reduce patient rejections and ensure adequate coverage during peak periods.
3.	Introduce attendance incentives, cross-department support programs, targeted workload management to maintain staff morale and prevent burnout. 
4.	Focus on reducing patients’ dissatisfaction by collecting service-related feedback and maintaining consistent care quality. 
5.	Monitor staff performance, patients flow, and bed occupancy in real-time to proactively attend to these challenges, prevent capacity shortages and optimize resource allocation.
    
## Conclusion
MERIT hospital management dashboard provides strong visibility into patient demand, service utilization, and workforce performance across the organization. While several services demonstrate effective admission handling and stable staff attendance, periods of high demand, elevated refusals, and fluctuating staff morale reveal operational pressure points. By improving capacity alignment, strengthening staffing coverage during peak periods, and closely monitoring morale alongside performance metrics, hospital management can convert existing operational effort into more efficient, patient-centered service delivery.








