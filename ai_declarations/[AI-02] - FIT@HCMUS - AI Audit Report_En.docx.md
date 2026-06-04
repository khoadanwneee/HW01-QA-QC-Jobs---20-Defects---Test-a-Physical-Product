**Faculty of Information Technology (FIT) – Ho Chi Minh City University of Science (HCMUS)**

**CS423 / CSC13003 – Software Testing (AI-augmented · 2026)**

**AI POLICY · TEMPLATES — 2026 v1.0**

# **AI Audit Report — 5-section Template per Artifact**

_Mandatory appendix for every AI-assisted homework (HW#01–HW#06, and Seminar)._

_Adapted from Med Kharbach, PhD (2026) — AI Use Policy Templates for Higher Education. CC BY-NC-SA 4.0. This adaptation is prepared for FIT@HCMUS – CS423 / CSC15003 Software Testing course._

## **1. Student Information**

| Field                                   | Value                             |
| :-------------------------------------- | :-------------------------------- |
| **Student name (printed):**             | Đặng Đăng Khoa                    |
| **Student ID:**                         | 23127207                          |
| **Class / Cohort:**                     | 23KTPM3                           |
| **Assignment ID (e.g., HW#00, HW#02):** | HW#01                             |
| **Assignment date:**                    | 04/06/2026                        |
| **AI tool(s) used:**                    | Gemini 1.5 Pro, Claude 3.5 Sonnet |
| **AI tool(s) used:**                    | [x] Yes [ ] No                    |

## **2. Instructions (read before filling)**

- Add one row per AI-generated artifact (test case, script, checklist, OpenAPI spec, JMeter plan, etc.).
- Paste the verbatim prompt — DO NOT paraphrase.
- Paste the verbatim AI output (or include a labelled screenshot in the report).
- Tag the verdict: VALID / INVALID / INCOMPLETE.
- Reasoning must cite a course slide, ISTQB section, or technical RFC.
- Show the corrected artifact with the change highlighted.
- Sample rows are in italic — replace them before submission.

## **3. Audit Table — one row per artifact**

| (1) Prompt + Tool                                                                                                                                           | (2) AI Output                                                                                                                                                   | (3) Verdict | (4) Reasoning (ISTQB)                                                                                                                            | (5) Student Fix                                                                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- | :----------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tool:** Gemini 1.5 Pro<br>**Time:** 20:15 03/06/2026<br>**Prompt:** "Tìm 10 tin tuyển dụng QA/QC đăng trong 60 ngày qua..."                               | _Generated 10 jobs with job descriptions and requirements. However, 8 of the generated job links were broken (404/Page Not Found)._                             | INCOMPLETE  | ISTQB FL §1.4.3: Traceability and accuracy of test information. AI failed to verify live resource links, creating false information.             | **Student Fix:** Manually searched for the actual job postings on LinkedIn and ITViec, replaced all broken links, and took date-verified screenshots showing my account.  |
| **Tool:** Claude 3.5 Sonnet<br>**Time:** 21:33 04/06/2026<br>**Prompt:** "Tìm 20 lỗi phần mềm thực tế được công bố trong giai đoạn 2022–2026..."            | _Generated 20 defects with descriptions, severity, and consequences. However, some links were unavailable and it hallucinates about platform responsibilities._ | INCOMPLETE  | ISTQB FL §2.1: Software defects classifications. The AI attributed configuration errors as core protocol defects (OIDC security trust policies). | **Student Fix:** Corrected all 404 links, aligned severity to ISTQB-defined standards, and highlighted specific instances of AI hallucination for all 20 defects.         |
| **Tool:** Gemini 1.5 Pro<br>**Time:** 23:08 04/06/2026<br>**Prompt:** "Hãy thiết kế 15 kịch bản kiểm thử (Test Cases) cho quạt đứng Asiavina D16022-DV0..." | _Generated 15 test cases. However, it only produced standard tests (On/Off, Speed levels) and completely missed physical and mechanical edge cases._            | INCOMPLETE  | ISTQB FL §4.2: Test design techniques. AI fails to incorporate environmental/dynamical constraints (mass distribution, cable tension).           | **Student Fix:** Added 3 advanced physical edge cases (TC09, TC10, TC11) manually, cleared AI-generated placeholder execution details, and ran actual physical test runs. |

## **4. Summary of AI Accuracy**

Aggregate the verdicts from Section 3 and complete the table below.

| Metric                                   | Count | Percentage |
| :--------------------------------------- | :---- | :--------- |
| **Total AI-generated artifacts audited** | 3     | 100%       |
| **VALID (correct, accepted as-is)**      | 0     | 0%         |
| **INVALID (wrong; rejected)**            | 0     | 0%         |
| **INCOMPLETE (acceptable after edits)**  | 3     | 100%       |

## **5. Conclusion — When should AI be used (or not)?**

AI tools like Gemini and Claude show strong capabilities in standard formatting, structural outlining, and boilerplate draft generation. However, AI lacks the contextual capability to verify live digital links or simulate complex 3D physical constraints (such as physical gravity displacement or wire tension forces in stand fan rotation). AI should be used primarily as an accelerator for brainstorming, structuring, and boilerplate drafting. It must NOT be used for direct factual lookup without rigorous manual verification of references, nor should it be trusted to design safety-critical physical test scenarios without human oversight.

## **6. Mandatory Disclosure (paste verbatim)**

_"Test cases was initially generated by Gemini; I reviewed and modified Section 3.1 and Section 3.2, added edge cases TC09, TC10, TC11; Section 3.3 and Section 4 were written entirely by me. The detailed AI Audit Report is attached as Appendix A. I confirm I did not use AI to generate any artifact listed in the prohibited category."_

## **Signature**

| Student name (printed): | Đặng Đăng Khoa                      |
| :---------------------- | :---------------------------------- |
| **Student ID:**         | 23127207                            |
| **Class / Cohort:**     | 23KTPM3                             |
| **Course:**             | CS423 / CSC13003 – Software Testing |
| **Instructor:**         | MSc. Tran Thi Bich Hanh             |
| **Date:**               | 04/06/2026                          |
| **Signature:**          | ![Signature](signature/signature.png) |

## **References**

- Kharbach, M. (2026). AI Use Policy Templates for Higher Education. CC BY-NC-SA 4.0.
- ISTQB Foundation Level Syllabus (latest version).
- Hardman, P. (2025). A Post-AI Learning Taxonomy.
- Fuster Rabella, M. (2025). OECD Education Working Paper No. 338.
- Perkins, M., Roe, J., & Furze, L. (2025). AI Assessment Scale.
- Anthropic (2025). Building reliable AI test agents — engineering blog.
- DeepEval & Promptfoo documentation — testing frameworks for LLM systems.
