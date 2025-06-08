# Lead-Assignment-Automation-with-Flow-Apex
Automatically assign incoming leads to the correct sales rep based on source or region using a combination of Flow and Apex

Use Case:
A company receives leads from various sources (Website, Trade Shows, Partners) and from multiple countries. The leads should be assigned to different sales reps based on region. If no one is available in that region, assign leads in a round-robin fashion among default fallback users.

Assignment Logic:

If Country = USA, assign to User A

If Country = UK, assign to User B

If no match, use Apex to round-robin between User C, User D, and User E

🛠 Tools Used
Flow Builder: To trigger automation on lead creation.

Custom Metadata: To define region-to-user mapping.

Apex: For fallback round-robin assignment.
