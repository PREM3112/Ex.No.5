
# EXP 5 – Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios

### DATE: 26.11.2026
### REGISTER NUMBER: 212223240124
### NAME: PREM R

## 1. AIM

To compare different prompting techniques and evaluate their effectiveness in solving real-world engineering problems using the final-year project **A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery: Design and Prototype Evaluation**.

## 2. AI TOOLS REQUIRED

- ChatGPT
- Google Gemini AI (project integration)

## 3. PROJECT TITLE

**A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery: Design and Prototype Evaluation**

## 4. PROBLEM STATEMENT

During medical emergencies, patients and their relatives often face difficulties in locating blood banks that have the required blood group and quantity available. Traditional blood resource discovery methods depend on manual phone calls, hospital visits and centralized databases.

These methods can result in delays, outdated inventory information and difficulties in identifying suitable blood banks.

Centralized blood inventory systems may also face challenges related to transparency, unauthorized data modification and data availability.

To address these challenges, a hybrid system combining Blockchain, InterPlanetary File System (IPFS) and Generative AI can be developed.

Blockchain provides an auditable record of authorized inventory updates, while IPFS supports off-chain storage of inventory information. Generative AI processes natural language requests and extracts structured search parameters.

The proposed system helps users discover registered blood banks that report the required blood group and quantity, subject to verification and location-based filtering.

Actual blood availability must be confirmed directly with the blood bank before proceeding with any medical decision.

## 5. SELECTED ENGINEERING SCENARIO

**Scenario:** Developing an emergency blood resource discovery system using Blockchain, IPFS and Generative AI.

**Input:** A natural language request containing the required blood group, quantity and urgency, along with the user's location when available.

**Example Input:**

"I urgently need two units of O+ blood near Chennai."

**Processing:**

- Extract structured information from the user request using Generative AI.
- Validate the extracted blood group, quantity and urgency.
- Retrieve registered blood bank information from the blockchain.
- Retrieve inventory records from IPFS.
- Filter blood banks based on verification status and reported inventory.
- Calculate the distance between the user and eligible blood banks.
- Display suitable blood bank results.

**Output:** A list of eligible blood banks with their reported blood availability, location, verification status and contact information.

**Technologies Used:**

- React Native
- TypeScript
- Google Gemini AI
- Solidity
- Ethereum Blockchain
- Sepolia Testnet
- IPFS
- Pinata
- Geoapify API
- React Native Maps
- JSON
- Node.js

## 6. BASE PROMPT (NAÏVE PROMPT)

**Prompt:**

Suggest a method to develop an emergency blood resource discovery system using Blockchain, IPFS and Generative AI.

**AI-Generated Output:**

An emergency blood resource discovery system can be developed by combining Blockchain technology, decentralized storage and artificial intelligence.

1. Register hospitals and blood banks on a blockchain network.
2. Store blood inventory information using IPFS.
3. Use smart contracts to manage blood bank registration and inventory updates.
4. Integrate an AI chatbot to understand user requests.
5. Search for blood banks that have the required blood group.
6. Display nearby blood banks using a map interface.
7. Provide contact information so users can confirm blood availability.

The proposed system can improve blood resource discovery by reducing manual searching and providing access to recorded inventory information.

However, additional verification mechanisms are required to ensure the accuracy of blood availability information.

## 7. IMPROVED PROMPTS USING DIFFERENT PROMPTING TECHNIQUES

### Technique 1 – Zero-Shot Prompting

**Prompt:**

Explain how to develop an emergency blood resource discovery system using Ethereum Blockchain, IPFS and Generative AI.

Describe the system architecture, smart contract design, blood bank registration process, inventory storage, natural language processing, location-based filtering and mobile application development.

Include suitable technologies, security mechanisms and testing methods without relying on example inputs or outputs.

**AI-Generated Output:**

An emergency blood resource discovery system can be developed using a hybrid decentralized architecture.

1. **System Architecture:** Divide the application into a mobile frontend, AI request processing module, blockchain registry, IPFS storage and location-based discovery module.

2. **Blood Bank Registration:** Register blood banks through Ethereum smart contracts using unique wallet addresses.

3. **Administrative Verification:** Allow authorized administrators to verify registered blood banks before their inventory becomes eligible for discovery.

4. **Inventory Storage:** Store blood inventory information as JSON files on IPFS and record the corresponding Content Identifier (CID) on the blockchain.

5. **AI Integration:** Use Google Gemini AI to extract the blood group, required quantity and urgency from natural language requests.

6. **Search and Filtering:** Retrieve inventory data and filter blood banks based on verification status, requested blood group and sufficient reported quantity.

7. **Location-Based Discovery:** Calculate geographical distances and display eligible blood banks in ascending distance order.

8. **Mobile Application:** Develop a React Native application to accept user requests and display blood banks through an interactive map.

9. **Security:** Implement role-based access control, input validation and restricted smart contract functions.

10. **Testing:** Evaluate smart contract authorization, AI extraction accuracy, inventory retrieval and search response time.

This architecture reduces the amount of inventory data stored directly on the blockchain while supporting auditable inventory updates.

### Technique 2 – Few-Shot Prompting

**Prompt:**

Develop an AI-based emergency blood resource discovery system using Blockchain and IPFS.

Follow the examples below to understand the expected structured extraction format.

Example 1:

Input:

"I urgently need two units of O+ blood."

Output:

{
  "bloodGroup": "O+",
  "quantity": 2,
  "urgency": "Emergency"
}

Example 2:

Input:

"Find three units of A- blood for a patient."

Output:

{
  "bloodGroup": "A-",
  "quantity": 3,
  "urgency": null
}

Example 3:

Input:

"I need blood immediately."

Output:

{
  "bloodGroup": null,
  "quantity": null,
  "urgency": "Emergency"
}

Now explain how to develop a system that extracts these parameters, validates missing information, retrieves blood inventory from IPFS, filters verified blood banks and displays suitable results.

Include error handling and practical implementation methods.

**AI-Generated Output:**

A structured natural language extraction system can be implemented using Google Gemini AI and JSON-based response formatting.

1. Accept natural language requests through the mobile application.

2. Provide predefined examples and a structured JSON schema to the AI model.

3. Extract the following parameters:

   - Blood group
   - Required quantity
   - Urgency

4. Validate the extracted blood group against the supported ABO and Rh blood groups.

5. Verify that the requested quantity is a positive integer.

6. If mandatory information is missing, request clarification instead of generating an assumed value.

7. Retrieve the registered blood bank addresses and corresponding inventory CIDs from the blockchain.

8. Fetch the inventory JSON files from IPFS.

9. Filter verified and active blood banks based on the exact requested blood group and sufficient reported quantity.

10. Rank eligible blood banks according to geographical distance when location information is available.

**Example Extraction Results:**

| User Input | Blood Group | Quantity | Urgency |
|---|---|---:|---|
| Need two units of O+ blood urgently | O+ | 2 | Emergency |
| Find three units of A- blood | A- | 3 | Not specified |
| Need AB+ blood immediately | AB+ | Not specified | Emergency |
| I need blood | Not specified | Not specified | Not specified |

The few-shot approach helps establish a consistent response format and reduces ambiguity in natural language extraction.

The system must handle malformed AI responses and missing information before initiating the discovery process.

### Technique 3 – Persona Pattern

**Prompt:**

Act as an experienced Blockchain Architect, Artificial Intelligence Engineer and Healthcare Software Developer.

You are assigned to develop an emergency blood resource discovery platform that combines Ethereum Blockchain, IPFS and Generative AI.

Design a practical and secure system using Solidity, React Native, TypeScript and Google Gemini AI.

Explain the system architecture, smart contract functions, decentralized inventory storage, AI request extraction, blood bank verification, location-based filtering, security mechanisms and performance evaluation.

Also discuss the technical challenges and limitations of implementing this system in real healthcare environments.

**AI-Generated Output:**

A hybrid blockchain-based blood resource discovery platform can be developed using a modular architecture.

1. **Frontend Development:**

   Develop a React Native application that allows users to submit natural language blood requests, view registered blood banks and access contact information.

2. **Generative AI Module:**

   Integrate Google Gemini AI to convert user requests into structured JSON containing blood group, quantity and urgency.

   The AI model should be restricted to information extraction rather than medical diagnosis or transfusion recommendations.

3. **Blockchain Module:**

   Develop Solidity smart contracts for managing:

   - Blood bank registration
   - Administrative verification
   - Authorized inventory updates
   - Inventory CID retrieval
   - Audit events

   Suggested smart contract functions:

   - registerBloodBank()
   - verifyBloodBank(address, bool)
   - updateInventory(...)

4. **IPFS Storage Module:**

   Store inventory records as JSON documents on IPFS using a pinning service such as Pinata.

   Store the corresponding CID on the blockchain instead of storing the entire inventory document directly on-chain.

5. **Discovery Module:**

   Filter blood banks based on:

   - Verification status
   - Active status
   - Exact requested blood group
   - Sufficient reported quantity
   - Inventory freshness, when supported

6. **Location Module:**

   Use geographical coordinates to calculate the distance between the user and eligible blood banks.

   Display the results through React Native Maps.

7. **Security Module:**

   Implement wallet-based authorization, administrative access control, input validation and protection of API credentials.

   Avoid storing sensitive patient information on a public blockchain or publicly accessible IPFS documents.

8. **Performance Evaluation:**

   Evaluate:

   - Blockchain transaction gas consumption
   - AI field extraction accuracy
   - API response latency
   - Smart contract authorization
   - Inventory filtering correctness

**Technical Challenges:**

- Outdated blood inventory information
- Blockchain transaction costs
- IPFS content availability
- AI extraction errors
- External API failures
- Unauthorized inventory updates
- Differences between reported and physical stock
- Internet connectivity limitations

Blockchain can record authorized inventory submissions, but it cannot independently confirm whether the reported blood stock physically exists.

Users must contact the selected blood bank to confirm availability.

### Technique 4 – Chain-of-Thought Prompting (Structured Step-by-Step Approach)

**Prompt:**

Analyze the engineering problem of emergency blood resource discovery using Blockchain, IPFS and Generative AI systematically.

Provide a structured engineering solution covering problem identification, requirement analysis, system architecture, smart contract development, inventory storage, AI information extraction, eligibility filtering, location-based ranking, testing and deployment.

For each stage, explain its purpose, selected method and expected outcome.

Include appropriate engineering evaluation metrics and practical limitations.

**AI-Generated Output:**

A systematic approach to developing an emergency blood resource discovery system involves the following stages.

**Step 1: Problem Identification**

Patients and their relatives may experience delays while searching for blood banks with the required blood group.

The proposed system provides a digital mechanism for discovering blood banks that report suitable inventory.

**Step 2: Requirement Analysis**

Identify the functional requirements of the system.

- Blood bank registration
- Administrative verification
- Inventory updates
- Natural language request processing
- Blood group and quantity filtering
- Location-based discovery
- Contact information display

Non-functional requirements include security, reliability, response time and usability.

**Step 3: System Architecture**

Develop a modular architecture consisting of:

- Mobile application
- Generative AI extraction module
- Ethereum smart contracts
- IPFS inventory storage
- Location-based discovery module

**Step 4: Smart Contract Development**

Use Solidity to implement blood bank registration, administrative verification and authorized inventory updates.

Restrict inventory modification to authorized participants.

Emit blockchain events for important registry operations.

**Step 5: Inventory Storage**

Represent blood inventory as structured JSON documents.

Upload the inventory documents to IPFS through Pinata.

Store the corresponding CID in the smart contract.

This reduces the amount of inventory information that must be stored directly on-chain.

**Step 6: AI Information Extraction**

Use Google Gemini AI to extract the required blood group, quantity and urgency from natural language requests.

Validate all extracted fields before forwarding them to the discovery module.

Request additional information if mandatory fields are missing.

**Step 7: Eligibility Filtering**

Retrieve the inventory of registered blood banks.

Apply the following conditions:

- The blood bank is verified.
- The blood bank is active.
- The requested blood group matches exactly.
- The reported stock is sufficient.

Exclude records that fail the eligibility conditions.

**Step 8: Location-Based Ranking**

Calculate the geographical distance between the user and eligible blood banks.

Sort the results by distance when valid location information is available.

Display contact information and inventory update information when supported.

**Step 9: System Evaluation**

Evaluate the system using:

- AI information extraction accuracy
- Smart contract authorization test results
- Blockchain gas consumption
- Search response latency
- Inventory filtering correctness
- Error handling performance

**Step 10: Deployment**

Deploy the smart contracts on the Sepolia Ethereum Testnet.

Integrate the contracts with the React Native mobile application.

Connect the application with Gemini AI, IPFS and mapping services.

Test the complete discovery workflow before considering real-world deployment.

The final system provides a structured approach to blood resource discovery while maintaining clear boundaries between reported inventory information and actual medical availability.

### Technique 5 – Role-Based and Constraint-Based Prompting

**Prompt:**

Act as an experienced Blockchain Architect and AI Systems Engineer.

Design a secure, cost-efficient and practical emergency blood resource discovery system using Ethereum Blockchain, IPFS, Google Gemini AI and React Native.

Consider the following constraints:

- Only authorized blood banks should update their inventory.
- Blood banks must be verified by an administrator.
- Complete inventory documents should be stored off-chain using IPFS.
- Only necessary registry information and inventory CIDs should be stored on-chain.
- Generative AI should extract information without providing medical advice.
- Missing mandatory information must not be guessed.
- Search results must use exact blood group matching.
- Blood banks must have sufficient reported stock.
- Only verified and active blood banks should appear in eligible results.
- Eligible blood banks should be ranked by distance when location is available.
- The system must handle API failures and unavailable IPFS content.
- Sensitive patient information must not be stored publicly.
- Actual blood availability must be confirmed directly with the blood bank.

Suggest a suitable architecture, implementation strategy, smart contract security mechanisms, AI validation methods, performance metrics and testing procedures.

**AI-Generated Output:**

A hybrid on-chain and off-chain architecture is recommended for developing a secure emergency blood resource discovery system.

**1. System Architecture**

The proposed architecture consists of five primary modules:

- React Native mobile application
- Generative AI extraction and validation module
- Ethereum smart contract registry
- IPFS inventory storage module
- Blood resource discovery and location module

**2. Blockchain Registry**

Use Solidity smart contracts to manage registered blood banks.

Each blood bank record should contain:

- Registered wallet address
- Blood bank identification information
- Administrative verification status
- Active status
- Inventory CID

Implement authorization checks to prevent unauthorized registration changes, verification and inventory updates.

**3. Hybrid IPFS Storage**

Store blood inventory documents on IPFS instead of storing every inventory field directly on the blockchain.

Example inventory document:

{
  "bloodBankId": "BB001",
  "inventory": {
    "A+": 5,
    "A-": 2,
    "B+": 4,
    "B-": 1,
    "AB+": 2,
    "AB-": 1,
    "O+": 8,
    "O-": 3
  },
  "lastUpdated": "2026-11-26T08:00:00Z"
}

The corresponding CID is recorded on the blockchain through an authorized inventory update.

IPFS pinning should be maintained to improve content availability. Independent CID verification should be implemented before relying on retrieved content in production.

**4. Generative AI Integration**

Use Google Gemini AI with a structured JSON response schema.

Example response:

{
  "bloodGroup": "O+",
  "quantity": 2,
  "urgency": "Emergency",
  "replyMessage": "Searching for blood banks reporting the requested inventory."
}

Validate the extracted information using deterministic application logic.

The AI model must not decide blood transfusion compatibility or generate medical treatment recommendations.

**5. Eligibility Filtering**

A blood bank is eligible only when all the following conditions are satisfied:

- Its registration is valid.
- Its verification status is true.
- Its active status is true.
- The requested blood group exists in the inventory.
- The reported quantity is greater than or equal to the requested quantity.

Inventory records that cannot be retrieved or validated should not be treated as confirmed eligible results.

**6. Location-Based Ranking**

Use the geographical coordinates of the user and eligible blood banks.

Calculate straight-line geographical distance using the Haversine formula.

Sort eligible blood banks from nearest to farthest.

Geographical distance should not be represented as actual road travel time.

**7. Error Handling**

The system should handle:

- Invalid blood groups
- Missing quantities
- Invalid JSON responses
- Gemini API quota errors
- Blockchain connection failures
- Unavailable IPFS documents
- Invalid geographical coordinates
- Insufficient reported inventory

Provide appropriate error messages instead of generating unverified results.

**8. Security and Privacy**

- Use role-based smart contract access control.
- Protect API keys through a secure backend.
- Prevent unauthorized inventory modifications.
- Validate retrieved inventory data.
- Avoid storing sensitive patient information on-chain.
- Maintain appropriate audit records.

**9. Performance Evaluation**

Evaluate the proposed system using:

- Gas consumption per inventory update
- AI extraction accuracy
- Mean response latency
- Smart contract authorization test success
- Inventory filtering correctness
- IPFS retrieval reliability

**10. Healthcare Safety**

The system should be presented as a blood resource discovery platform rather than a clinical decision-support system.

Users must confirm current blood availability directly with the selected blood bank.

Medical professionals must determine patient eligibility, blood compatibility and transfusion requirements.

This approach provides a practical engineering solution while considering security, implementation cost, data integrity and healthcare safety.

## 8. COMPARISON OF PROMPTING TECHNIQUES

| Prompting Technique | Quality | Accuracy | Depth |
|---|---|---|---|
| Naïve Prompt | Basic | General information | Low |
| Zero-Shot Prompting | Good | Relevant technical suggestions | Medium |
| Few-Shot Prompting | Very Good | Consistent structured extraction | High |
| Persona Pattern | Very Good | Engineering-focused recommendations | High |
| Chain-of-Thought Prompting | Very Good | Systematic implementation approach | Very High |
| Role-Based and Constraint-Based Prompting | Excellent | Considers technical and safety constraints | Very High |

## 9. EVALUATION TABLE

The following scores represent qualitative assessments of the generated responses.

Each criterion is evaluated using a scale of 1 to 5.

- 1 – Poor
- 2 – Fair
- 3 – Satisfactory
- 4 – Very Good
- 5 – Excellent

| Evaluation Criteria | Naïve | Zero-Shot | Few-Shot | Persona | Chain-of-Thought | Constraint-Based |
|---|---:|---:|---:|---:|---:|---:|
| Relevance | 4 | 4 | 5 | 5 | 5 | 5 |
| Accuracy | 3 | 4 | 4 | 4 | 4 | 5 |
| Completeness | 2 | 4 | 4 | 5 | 5 | 5 |
| Clarity | 4 | 4 | 5 | 5 | 5 | 5 |
| Feasibility | 3 | 4 | 4 | 4 | 5 | 5 |
| Usefulness | 3 | 4 | 5 | 5 | 5 | 5 |
| **Total (30)** | **19** | **24** | **27** | **28** | **29** | **30** |
| **Percentage** | **63.33%** | **80%** | **90%** | **93.33%** | **96.67%** | **100%** |
| **Rank** | **6** | **5** | **4** | **3** | **2** | **1** |

The scores evaluate the relevance and quality of the written responses within the selected rubric. They do not represent independently measured AI accuracy or clinical performance.

## 10. ANALYSIS AND OBSERVATIONS

The experiment demonstrates that the quality of AI-generated responses depends on the clarity, structure and technical specificity of the prompt.

### 10.1 Naïve Prompting

The naïve prompt produces a general overview of the proposed system.

**Advantages:**

- Easy to formulate.
- Requires minimal input.
- Suitable for initial brainstorming.

**Limitations:**

- Lacks detailed implementation guidance.
- Does not adequately address security.
- Provides limited validation procedures.
- Does not specify important healthcare constraints.

### 10.2 Zero-Shot Prompting

Zero-shot prompting produces a more detailed technical response by explicitly describing the expected components.

**Advantages:**

- Provides relevant system architecture.
- Identifies suitable technologies.
- Explains implementation modules without examples.

**Limitations:**

- Does not establish a consistent AI extraction format through examples.
- May overlook specific edge cases.

### 10.3 Few-Shot Prompting

Few-shot prompting improves the consistency of structured AI outputs by providing representative input-output examples.

**Advantages:**

- Supports consistent JSON formatting.
- Improves understanding of expected outputs.
- Demonstrates handling of missing information.
- Particularly suitable for the Generative AI extraction module.

**Limitations:**

- Requires carefully selected examples.
- Incorrect examples may influence subsequent responses.
- Does not automatically guarantee complete system architecture.

### 10.4 Persona Pattern

Persona prompting encourages the AI system to respond from the perspective of an experienced engineering professional.

**Advantages:**

- Produces domain-specific recommendations.
- Considers security and implementation challenges.
- Provides professional engineering explanations.
- Identifies limitations of blockchain-based inventory systems.

**Limitations:**

- Assigning a professional role does not guarantee factual accuracy.
- Recommendations still require technical validation.

### 10.5 Chain-of-Thought Prompting

The structured step-by-step approach organizes the engineering solution into logical implementation stages.

**Advantages:**

- Improves clarity and organization.
- Explains the purpose of individual modules.
- Provides a systematic implementation sequence.
- Supports project planning and testing.

**Limitations:**

- Produces comparatively lengthy responses.
- May not prioritize project-specific constraints unless they are explicitly included.

### 10.6 Role-Based and Constraint-Based Prompting

This technique combines professional role assignment with clearly defined technical requirements and operational restrictions.

**Advantages:**

- Provides comprehensive engineering recommendations.
- Considers project-specific requirements.
- Addresses security and privacy.
- Includes error handling and validation procedures.
- Establishes healthcare safety boundaries.
- Improves practical implementation feasibility.

**Limitations:**

- Requires a clear understanding of project requirements.
- Takes more effort to formulate.
- Incorrect or incomplete constraints may affect the generated solution.

### 10.7 Naïve Versus Improved Prompt Comparison

| Parameter | Naïve Prompt | Improved Prompt |
|---|---|---|
| System Architecture | General overview | Detailed modular architecture |
| Blockchain Integration | Basic explanation | Smart contract functions and authorization |
| IPFS Integration | General storage suggestion | Structured inventory documents and CID management |
| AI Integration | Basic chatbot concept | Validated JSON information extraction |
| Blood Bank Verification | Limited explanation | Administrative verification and active status |
| Inventory Filtering | General matching | Exact blood group and quantity validation |
| Security | Limited | Role-based access control and privacy |
| Error Handling | Mostly absent | API, validation and storage failure handling |
| Performance Evaluation | Limited metrics | Gas, extraction accuracy and latency |
| Healthcare Safety | Basic guidance | Clearly defined clinical limitations |
| Implementation Feasibility | Moderate | High |

### Does ChatGPT consistently provide better results with improved prompts?

In the evaluated sample responses, improved prompts generally produced more relevant, detailed and structured engineering solutions than the naïve prompt.

However, naïve prompts can also produce satisfactory responses when the problem is straightforward or when only a brief conceptual explanation is required.

For complex engineering projects involving Blockchain, Generative AI and healthcare applications, structured prompts are more useful because they explicitly define implementation requirements, technical constraints and safety considerations.

The experiment does not establish that longer prompts always produce better results. Prompt effectiveness depends on the relevance and correctness of the information provided.

## 11. FINAL SELECTED PROMPTING TECHNIQUE

**Selected Technique: Role-Based and Constraint-Based Prompting**

Role-Based and Constraint-Based Prompting was selected as the most suitable technique for the engineering problem.

This technique achieved the highest qualitative evaluation score of 30 out of 30 within the selected assessment rubric.

It was selected because it:

1. Provides a complete system architecture.
2. Considers blockchain authorization requirements.
3. Supports cost-efficient off-chain inventory storage.
4. Defines structured Generative AI information extraction.
5. Addresses missing and invalid input information.
6. Incorporates blood bank verification and inventory filtering.
7. Includes location-based discovery.
8. Provides security and privacy recommendations.
9. Defines measurable performance evaluation criteria.
10. Recognizes the limitations of blood resource discovery systems.

Few-shot prompting can additionally be combined with this technique to improve the consistency of the Generative AI extraction module.

## 12. REFINED / FINAL PROMPT

Act as an experienced Blockchain Architect, Artificial Intelligence Engineer and Healthcare Software Developer.

I am developing a final-year engineering project titled:

"A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery: Design and Prototype Evaluation."

The objective is to develop a secure and practical blood resource discovery system that helps users locate verified blood banks reporting the required blood group and quantity.

Design a modular implementation using Solidity, Ethereum Blockchain, Sepolia Testnet, IPFS, Pinata, Google Gemini AI, React Native, TypeScript and location-based services.

Consider the following requirements:

1. Develop an Ethereum smart contract for blood bank registration and administrative verification.

2. Restrict inventory updates to authorized blood bank wallets.

3. Store detailed inventory information as JSON documents on IPFS.

4. Store the corresponding inventory CID on the blockchain.

5. Use Google Gemini AI to extract blood group, quantity and urgency from natural language requests.

6. Generate structured JSON responses using the following fields:

   - bloodGroup
   - quantity
   - urgency
   - replyMessage

7. Validate all extracted fields using deterministic application logic.

8. Request clarification when mandatory information is missing.

9. Filter blood banks using exact blood group matching, sufficient reported quantity, verification status and active status.

10. Calculate geographical distance and rank eligible blood banks when location information is available.

11. Display blood bank information and contact details through a React Native mobile application.

12. Handle invalid inputs, malformed JSON responses, API quota errors, blockchain failures and unavailable IPFS content.

13. Implement role-based authorization, secure API credential management and patient privacy protection.

14. Evaluate the proposed system using blockchain gas consumption, AI extraction accuracy, response latency, authorization test results and filtering correctness.

15. Explain the limitations of blockchain-based inventory records and distinguish reported stock from independently verified physical stock.

16. Restrict Generative AI to request extraction and prevent it from providing medical diagnosis, blood compatibility decisions or treatment recommendations.

17. Provide a modular implementation plan, architecture, validation strategy and expected outcomes.

Do not invent experimental results or claim that blood availability has been independently confirmed.

Clearly distinguish implemented features, proposed improvements and features requiring further validation.

Provide the solution in a structured engineering format with practical implementation details.

## 13. ENGINEERING VALIDATION

The proposed solution can be validated through functional, performance, security and integration testing.

### 13.1 Functional Validation

Verify that each system component performs its expected operation.

| Test ID | Test Case | Expected Result |
|---|---|---|
| TC01 | Register a blood bank using a valid wallet | Registration succeeds |
| TC02 | Verify a blood bank using an administrator wallet | Verification succeeds |
| TC03 | Attempt verification using an unauthorized wallet | Transaction is rejected |
| TC04 | Update inventory using an authorized wallet | Inventory CID is updated |
| TC05 | Attempt an unauthorized inventory update | Transaction is rejected |
| TC06 | Submit a valid natural language request | Required fields are extracted |
| TC07 | Submit a request without blood group | System requests clarification |
| TC08 | Submit a request without quantity | System requests clarification |
| TC09 | Submit an invalid blood group | Invalid input is rejected |
| TC10 | Search for sufficient reported inventory | Eligible blood banks are returned |
| TC11 | Search for insufficient inventory | Ineligible blood banks are excluded |
| TC12 | Search for an unverified blood bank | Blood bank is excluded |
| TC13 | Search for an inactive blood bank | Blood bank is excluded |
| TC14 | Retrieve an unavailable IPFS document | Retrieval error is handled |
| TC15 | Search multiple eligible blood banks | Results are ranked by distance |

These test cases describe the expected behavior of the proposed complete architecture. They should not be interpreted as executed test results unless corresponding execution evidence is available.

### 13.2 Blockchain Performance Validation

Compare the gas consumption of direct on-chain inventory storage with hybrid Blockchain–IPFS inventory storage.

The following measurements were reported in the project's prototype evaluation:

| Inventory Workload | Direct On-Chain Storage | Hybrid Blockchain–IPFS | Gas Reduction |
|---|---:|---:|---:|
| Small inventory update | 53,447 gas | 47,817 gas | 10.53% |
| Large inventory update | 68,731 gas | 47,817 gas | 30.43% |

**Gas Reduction Formula:**

Gas Reduction (%) = ((Baseline Gas - Hybrid Gas) / Baseline Gas) × 100

**Observation:**

The hybrid architecture reduced gas consumption for the two evaluated inventory workloads by storing inventory documents off-chain and recording the corresponding CID on-chain.

The measured reductions apply to the tested smart contract implementation and workloads.

### 13.3 Generative AI Validation

Evaluate the ability of the AI model to extract structured information from natural language blood requests.

The project's prototype evaluation reported the following results:

| Evaluation Parameter | Reported Result |
|---|---|
| Successfully processed English queries | 50 |
| Total processing attempts | 52 |
| API quota interruptions | 2 |
| Correct blood group extraction | 50/50 |
| Correct quantity extraction | 50/50 |
| Correct urgency extraction | 50/50 |
| Field extraction accuracy for completed queries | 100% |

**Observation:**

The evaluated English queries were successfully converted into the required structured fields.

However, the result is limited to the tested dataset and completed requests. It does not establish equivalent performance for multilingual queries, unseen request patterns or real-world clinical situations.

### 13.4 Smart Contract Security Validation

Evaluate access control and authorization mechanisms.

| Evaluation Parameter | Reported Result |
|---|---|
| Local authorization checks | 10 |
| Successful checks | 10 |
| Failed checks | 0 |
| Authorization test success rate | 100% |

**Observation:**

The reported authorization checks produced the expected results within the local test environment.

This evaluation does not replace an independent smart contract security audit.

### 13.5 Response Latency Validation

Measure the time required for the mobile application request handler to process user requests.

| Evaluation Parameter | Reported Result |
|---|---|
| Number of timing trials | 5 |
| Mean response latency | 1,550.37 ms |
| Standard deviation | 231.10 ms |
| Trials completed within 1,550.37 ms | 3/5 |
| Trials completed within 1,900.03 ms | 5/5 |

**Observation:**

The measured response latency provides an initial indication of prototype responsiveness under the evaluated conditions.

A larger number of trials under different network and workload conditions is required to establish reliable production-level performance.

### 13.6 Inventory Filtering Validation

Consider the following synthetic inventory records for an illustrative validation scenario.

User Request:

"I urgently need two units of O+ blood."

| Blood Bank | Verified | Active | O+ Stock | Distance | Expected Result |
|---|---|---|---:|---|---|
| Blood Bank A | Yes | Yes | 5 | 2 km | Eligible |
| Blood Bank B | Yes | Yes | 1 | 1 km | Insufficient stock |
| Blood Bank C | No | Yes | 8 | 3 km | Unverified |
| Blood Bank D | Yes | No | 6 | 4 km | Inactive |
| Blood Bank E | Yes | Yes | 4 | 5 km | Eligible |

**Expected Ranked Output:**

| Rank | Blood Bank | Blood Group | Reported Stock | Distance |
|---:|---|---|---:|---|
| 1 | Blood Bank A | O+ | 5 units | 2 km |
| 2 | Blood Bank E | O+ | 4 units | 5 km |

**Observation:**

Blood Bank A and Blood Bank E satisfy all the proposed eligibility conditions.

Although Blood Bank B is geographically closer, it is excluded because the reported quantity is insufficient.

Blood Bank C and Blood Bank D are excluded because they do not satisfy verification and active status requirements.

This example demonstrates the intended filtering logic using synthetic records rather than actual hospital inventory.

### 13.7 Engineering Limitations

The following limitations must be considered:

- Blockchain records authorized inventory submissions but does not independently verify physical blood stock.
- IPFS content availability depends on successful storage, pinning and retrieval.
- Independent CID verification requires further implementation and validation.
- The complete discovery workflow must consistently enforce all eligibility conditions.
- Quantitative AI evaluation was limited to English-language requests.
- API quota limitations may interrupt AI processing.
- Production-level scalability requires additional testing.
- Clinical accuracy and transfusion compatibility are outside the validated scope.
- Actual blood availability must be confirmed directly with the blood bank.

### Expected Outcome

The proposed system should provide a secure and structured method for discovering eligible blood banks based on recorded inventory information.

The prototype measurements support the feasibility of hybrid inventory storage and structured AI extraction within the tested conditions.

Further integration, security, usability and hospital-led validation are required before real-world clinical deployment.

## 14. OUTPUT

The different prompting techniques were applied to the selected engineering problem, and their generated responses were compared.

| Prompting Technique | Total Score | Percentage |
|---|---:|---:|
| Naïve Prompting | 19/30 | 63.33% |
| Zero-Shot Prompting | 24/30 | 80% |
| Few-Shot Prompting | 27/30 | 90% |
| Persona Pattern | 28/30 | 93.33% |
| Chain-of-Thought Prompting | 29/30 | 96.67% |
| Role-Based and Constraint-Based Prompting | 30/30 | 100% |

**Best Prompting Technique:** Role-Based and Constraint-Based Prompting.

**Selected Engineering Solution:** A hybrid Blockchain–IPFS architecture integrated with Generative AI for structured blood request extraction and location-based blood resource discovery.

**Major Observations:**

- Structured prompts produced more comprehensive engineering responses.
- Few-shot prompting improved the consistency of expected JSON outputs.
- Persona prompting provided domain-specific technical recommendations.
- Step-by-step prompting improved implementation organization.
- Constraint-based prompting addressed security, feasibility, privacy and healthcare safety.
- The proposed engineering solutions require validation before real-world deployment.

## 15. CONCLUSION

Thus, different prompting techniques were applied to the engineering problem of emergency blood resource discovery using Blockchain, IPFS and Generative AI.

The generated responses were compared based on relevance, accuracy, completeness, clarity, feasibility and usefulness.

The experiment demonstrated that structured prompting techniques can produce more detailed and practical engineering solutions than a simple naïve prompt.

Few-Shot Prompting was particularly useful for defining consistent structured AI extraction outputs, while Persona Pattern provided engineering-oriented recommendations.

The structured step-by-step approach helped organize the system development process into logical implementation stages.

Among the evaluated techniques, Role-Based and Constraint-Based Prompting provided the most comprehensive response because it considered technical requirements, blockchain authorization, inventory storage efficiency, AI validation, security, privacy and healthcare safety.

The experiment also established the importance of engineering validation rather than directly accepting AI-generated recommendations.

Therefore, combining clear role assignment, project context, technical constraints, representative examples and measurable evaluation criteria is an effective approach to obtaining useful AI-generated engineering solutions.

## RESULT

The experiment was executed successfully by applying and comparing different prompting techniques to the selected engineering problem, **A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery: Design and Prototype Evaluation**.

Based on the qualitative evaluation, Role-Based and Constraint-Based Prompting was identified as the most suitable prompting technique for the selected engineering scenario.
