
# Jobs4U Project 

---

## 1. User

| Context                          | Important Fields                                      |
|----------------------------------|-------------------------------------------------------|
|  user system                     | ID, user_login, user_email, user_pass, user_registered |
| Job application linkage          | userId , name, email, contact       |
| Commenting and interaction       | user_id, user roles, display_name |

---

## 2. Job

| Context                          | Important Fields                                                     |
|----------------------------------|----------------------------------------------------------------------|
| Job listings                     | ID (post ID), post_title, post_content, post_date, post_type='job'   |
| extra job details                | job_location, salary, company_name, job_type                         |
| Saved jobs                       | Potentially tracked  or a custom saved_jobs table (not yet seen)     |

---

## 3. Application

| Context                         | Important Fields                                           |
|----------------------------------|------------------------------------------------------------|
| Application submission           | ID, userId, jobID, firstName, LastName, email, contact, resume, comment |
| Resume handling                  | resume (file path or filename), stored in `job4U_apply`    |
| Linking user to job              | jobID ↔ post_id, userId ↔ WordPress user                   |

---

## 4. Comment

| Context                         | Important Fields                                                |
|----------------------------------|-----------------------------------------------------------------|
| Job or blog discussions          | comment_ID, comment_post_ID, comment_content, comment_author, comment_date |
| Comment moderation               | comment_approved, comment_status, user_id                      |
| Extra metadata                   | Stored in `job4U_commentmeta`                                   |

---

## 5. Subscriber

| Context                         | Important Fields                            |
|----------------------------------|---------------------------------------------|
| Job alerts or newsletters        | id, email, status (active/inactive)         |
| Not necessarily a registered user | subscriber data stored in `job4U_subscribers` |

---



## 6. Post Metadata

| Context                         | Important Fields                                                  |
|----------------------------------|-------------------------------------------------------------------|
| Extra data for job posts         | post_id, meta_key (e.g. salary, skills), meta_value               |
| Used for filtering/sorting       | Custom fields like `location`, `industry`, etc. in `job4U_postmeta` |

---

## 7. Recommendation Potential (Implied)

| Context                            | Important Fields (implied/inferred)                          |
|-------------------------------------|---------------------------------------------------------------|
| Related job suggestions             | User location (city), skills (if stored), past applied jobs   |
| WordPress plugin or custom engine   | Not directly visible, may depend on `postmeta`, `usermeta`, or plugin logic |

---


