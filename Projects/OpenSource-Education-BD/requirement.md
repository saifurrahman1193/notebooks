
# 📘 **Knowledge**

**Motto:**

> *Learn → Grow → Spread*

---

## 🗄️ Database

**DBMS:** MySQL

---

## 🧩 Panels

### 👥 Guest / Student / Teacher

* **API**
* **Frontend**

### 🛠️ Admin Panel

* **API**
* **Frontend**

---

## 🌐 Features

* **Language Support**

  * 🇧🇩 **Bangla** *(Default)*
  * 🇬🇧 **English***

---

## 🏫 Class Structure

### Class 9

#### Subject

* **Chapter**

  * **Paragraph**

    * Figure
    * Table
  * **Example**

    * **MCQ**

      * MCQ Options

        * Figure
    * **Example**

      * Example Figure
      * Example Table
    * **Exercise**

      * Exercise Figure
      * Exercise Table

---

## 🧮 Database Tables

| #  | Table                            | Description / Columns                                                                                                                                                                                                      |
| -- | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | **class/grade**                  | id, grade, grade_bn, grade_type_id, examination_id                                                                                                                                                                         |
| 2  | **grade_type**                   | id, grade_type (Primary, Secondary, Higher Secondary)                                                                                                                                                                      |
| 3  | **subject**                      | id, subject, subject_bn, grade_id, subject_code                                                                                                                                                                            |
| 4  | **chapter**                      | id, subject_id, chapter, chapter_bn, title, title_bn, page_ref                                                                                                                                                             |
| 5  | **paragraph**                    | id, paragraph, paragraph_bn, paragraph_title, paragraph_title_bn, chapter_id, parent_id, page_ref                                                                                                                          |
| 6  | **figure**                       | id, figure_path, figure_number, figure_number_bn, figure_title, figure_title_bn, paragraph_id                                                                                                                              |
| 7  | **table**                        | id, table_number, table_number_bn, table_title, table_title_bn, table_content, table_content_bn, paragraph_id                                                                                                              |
| 8  | **example**                      | id, chapter_id, example, example_bn, parent_id, serial, page_ref                                                                                                                                                           |
| 9  | **exam_ques**                    | id, example_id, exercise_id, education_board_id, exam_year, question_id, examination_id, question, question_bn, question_key, question_key_bn, parent_id                                                                   |
| 10 | **subj_ques**                    | id, question, question_bn, question_key, question_key_bn, subject_id, grade_id, chapter_id, parent_id, page_ref                                                                                                            |
| 11 | **subj_ques_ans**                | id, subject_question_id, answer, answer_bn, page_ref                                                                                                                                                                       |
| 12 | **subj_ques_ans_explan**         | id, subj_ques_id, subj_ques_ans_id, explanation, explanation_bn                                                                                                                                                            |
| 13 | **characteristics**              | id, exam_ques_id, subj_ques_id, paragraph_id, characteristic, description                                                                                                                                                  |
| 14 | **education_board**              | id, education_board, education_board_bn                                                                                                                                                                                    |
| 15 | **exercise**                     | id, chapter_id, exercise, exercise_bn, parent_id, serial, marks                                                                                                                                                            |
| 16 | **MCQ**                          | id, mcq, mcq_bn, chapter_id, subject_id, grade_id, serial                                                                                                                                                                  |
| 17 | **MCQ_options**                  | id, mcq_id, option_key, option_key_bn, option, option_bn, is_answer, serial                                                                                                                                                |
| 18 | **comment**                      | id, comment, exercise_id, example_id, paragraph_id, youtube_link, video_link, website_link, content_title, serial                                                                                                          |
| 19 | **comment_vote**                 | id, comment_id, vote_type_id, voter_id                                                                                                                                                                                     |
| 20 | **examination**                  | id, examination, examination_bn                                                                                                                                                                                            |
| 21 | **group**                        | id, group_name, group_name_bn                                                                                                                                                                                              |
| 22 | **subj_exam_group**              | id, subject_id, group_id, examination_id                                                                                                                                                                                   |
| 23 | **student**                      | id, user_id, institution_id                                                                                                                                                                                                |
| 24 | **teacher**                      | id, user_id, institution_id, is_verified                                                                                                                                                                                   |
| 25 | **teacher_subject**              | id, teacher_id, subject_id, grade_id                                                                                                                                                                                       |
| 26 | **education_qualification**      | id, qualification_title, institution_id, start_year, start_month, end_year, end_month, user_id, CGPA, CGPA_out_of                                                                                                          |
| 27 | **institution**                  | id, institution, contact_number, contact_person, email, address                                                                                                                                                            |
| 28 | **education_board_rank**         | id, education_board_id, rank, examination_id                                                                                                                                                                               |
| 29 | **users**                        | id, name, email, phone, password                                                                                                                                                                                           |
| 30 | **user_dtl**                     | id, user_id, division_id, city_id, district_id, area_id, dob, address, gender_id, nid, passport                                                                                                                            |
| 31 | **gender**                       | id, gender                                                                                                                                                                                                                 |
| 32 | **division**                     | id, division                                                                                                                                                                                                               |
| 33 | **district**                     | id, district, division_id                                                                                                                                                                                                  |
| 34 | **city**                         | id, city                                                                                                                                                                                                                   |
| 35 | **area**                         | id, area                                                                                                                                                                                                                   |
| 36 | **reputation**                   | id, reputation, reputation_type_id, owner_id, example_id, exercise_id, comment_id, chapter_id, subject_id, paragraph_id, grade_id                                                                                          |
| 37 | **reputation_type**              | id, reputation_type (answer, valid_answer, vote, wrong_answer, spam)                                                                                                                                                       |
| 38 | **vote_type**                    | id, vote_type (up vote, down vote)                                                                                                                                                                                         |
| 39 | **bookmark**                     | id, bookmarker_id, exercise_id, example_id, chapter_id, subject_id                                                                                                                                                         |
| 40 | **notification**                 | id, message, message_bn, notification_for                                                                                                                                                                                  |
| 41 | **badge**                        | id, badge, badge_bn                                                                                                                                                                                                        |
| 42 | **exam_routine**                 | id, title, grade_id, group_id, owner_id                                                                                                                                                                                    |
| 43 | **exam_routine_dtl**             | id, exam_routine_id, subject_id, date, seat_plan, exam_time_start, exam_time_end                                                                                                                                           |
| 44 | **visit**                        | id, check_in_time, check_out_time, visitor_id, subject_id, chapter_id, figure_id, table_id, paragraph_id, example_id, exercise_id, gender_id, city_id, division_id, district_id, area_id, mcq_id, grade_id, institution_id |
| 45 | **sms_log**                      | id, sms, sms_status_id, sender_id, receiver_id, msisdn, logtime, charge_amount                                                                                                                                             |
| 46 | **sms_status**                   | id, status                                                                                                                                                                                                                 |
| 47 | **credit**                       | id, user_id, credit_amount                                                                                                                                                                                                 |
| 48 | **credit_spending**              | id, logtime, credit_spending_purpose_id                                                                                                                                                                                    |
| 49 | **credit_spending_purpose**      | id, purpose                                                                                                                                                                                                                |
| 50 | **recharge**                     | id, recharge_status_id                                                                                                                                                                                                     |
| 51 | **recharge_status**              | id, status                                                                                                                                                                                                                 |
| 52 | **membership**                   | id, validity_start, validity_end, status, member_id                                                                                                                                                                        |
| 53 | **membership_status**            | id, status (active, inactive, blocked)                                                                                                                                                                                     |
| 54 | **membership_plan**              | id, title, title_bn, validity_days, charge_amount                                                                                                                                                                          |
| 55 | **whats_new**                    | id, title, title_bn, status                                                                                                                                                                                                |
| 56 | **whats_new_status**             | id, status                                                                                                                                                                                                                 |
| 57 | **comm_verify**                  | id, verifier_id, verified_at, comment_id, chapter_id, paragraph_id, example_id, exercise_id                                                                                                                                |
| 58 | **teacher_verification_level**   | id, level, comment_verification_point                                                                                                                                                                                      |
| 59 | **teacher_verification**         | id, user_id, teacher_id, verified_at, is_verified, comment                                                                                                                                                                 |
| 60 | **teacher_verification_request** | id, user_id                                                                                                                                                                                                                |
| 61 | **teacher_verification_history** | id, user_id, logtime                                                                                                                                                                                                       |
| 62 | **parent**                       | id, user_id, relationship_id                                                                                                                                                                                               |
| 63 | **relationship**                 | id, relationship                                                                                                                                                                                                           |

---

## 🧠 Core Features

* 🧩 **Quiz System**
* 🏆 **Leaderboard** (Teacher, Student)
* 📈 **Progress Chart** (Mark-wise, GPA-wise)
* 📄 **Lecture Sheets** (PDF/Word)

  * Single Chapter
  * Multiple Chapters
  * Bookmarks
* 📅 **Routine Maker**
* 💬 **Commenting System**
* 📚 **PDF Whole Book with Comments (Paid)**
* 💳 **Membership System**
* 📲 **SMS System** *(1tk per SMS)*

  * Student Attendance → Parents Notification
* 📅 **Attendance Panel**

  * Daily Report
  * Weekly/Monthly/Yearly (Paid)
  * Grade/Section Wise
* 🧍‍♂️ **User Privacy Controls**

  * Hide full name, phone, address, email
* 🏫 **Page Lists**

  * Teacher List (Institute, Approved Comments, Uploaded Videos)
  * Student List (Institute, Uploaded Videos, Comments)
  * Institution List (with Teacher List)
* 👩‍🏫 **Teacher Profile**
* 👨‍🎓 **Student Profile**
* 🖼️ **Profile Image Replacement**
* 🆕 **What's New Section**
* ⚡ **One Click Setup**

  * Group-wise Book Enlisting
  * Grade-wise Book Enlisting

---

Would you like me to make this **Markdown downloadable** (e.g., `.md` file)?
