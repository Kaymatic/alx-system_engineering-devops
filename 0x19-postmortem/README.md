INCIDENT REPORT

Incident Summary

Duration of Outage: December 10, 2023, 3:00 PM - 6:00 PM GMT
Impact: The FoodSaver platform was inaccessible, preventing users from viewing food listings or submitting requests and restaurants from posting new surplus food items. Approximately 500 users were affected.
Root Cause: A null pointer exception introduced by a recent code update in the API handling food listing retrieval caused the backend server to crash repeatedly.

Timeline

2:50 PM: Code update deployed to production.
3:00 PM: Users began reporting issues accessing food listings.
3:10 PM: Initial investigation started following monitoring alerts and user reports.
3:30 PM: Backend logs identified a null pointer exception causing server crashes.
4:00 PM: Decision made to rollback to the previous stable version.
4:30 PM: Rollback completed, restoring initial functionality.
5:00 PM: Thorough testing conducted to ensure no further issues.
6:00 PM: Full platform functionality confirmed, incident resolved.

Root Cause and Resolution

Root Cause : The outage was caused by a bug in the backend server code. A recent update introduced a null pointer exception in the API responsible for food listing retrieval. This exception occurred during the processing of certain database queries, leading to repeated server crashes and preventing the platform from serving user requests.
Resolution : The resolution involved rolling back to the previous stable version of the backend server code. Additional logging was implemented to capture detailed error information in the future. The recent code changes were reviewed comprehensively to identify and rectify the bug. Enhanced testing protocols were put in place to cover more extensive scenarios and prevent similar issues.

Corrective and Preventative Measures
Improvements and Fixes

CI/CD Pipeline: Improve the CI/CD pipeline to include more rigorous automated tests, focusing on edge cases and null pointer exceptions.
Code Review Process: Institute a mandatory code review process for all future updates to catch potential issues early.
Monitoring and Logging: Enhance logging to capture detailed information on errors and improve monitoring to detect issues more proactively.
Regular Audits: Schedule regular audits of critical systems and code dependencies to identify and address potential problems preemptively.

Tasks

Patch Backend Server Code: Ensure the current version is stable and bug-free.
Implement Detailed Logging: Add logging to capture detailed error information for future troubleshooting.
Review Code Changes: Conduct a thorough review of recent and future code changes to identify and fix potential issues.
Enhance Automated Testing: Expand automated tests to cover a wider range of scenarios, including edge cases.
Conduct Team Training: Train the development team on best practices for error handling and code reviews.

Conclusion

By implementing these corrective measures, we aim to prevent similar incidents in the future and ensure the stability and reliability of the FoodSaver platform. This incident highlighted the importance of robust testing and vigilant monitoring, and the team's swift response ensured a timely resolution, minimizing the impact on our users. Moving forward, we are committed to continuous improvement to prevent similar issues and enhance the overall user experience.


