# CHANGELOG

The changelog for the [model course repository](https://github.com/cslmath/model-Courses).

## 2025-09-20

Update all $formatedDueDate references to $formattedDueDate

## 2025-01-13

* Create model201-SC2 from model201-203 in such a way that the git history of both models
  (`git blame` etc) is preserved.
* Create model201-SN2, model201-SN3, model201-SN4
  from model201-NYA, model201-NYB, model201-NYC respectively.
* Update `model-include-from` for the new models.
* Start keeping track of notes of procedures in `notes.md`.
* Create the README and course_info.txt in models 201-SC2, 201-SN2, 201-SN3, 201-SN4.
* Tweak the README and course_info.txt in models 201-SC1 and 201-SLA.

## 2025-01-12

* Track `model-include-from` and `model-exclude-from`
  which enable syncing from the model courses on the server into this git repository.
  `rsync -avv --include-from=model-include-from --exclude-from=model-exclude-from /opt/webwork/courses/* ./`
  will copy the tracked files from the courses directory into . for tracking.
* Exclude the tmpEdit directories from tracking.
* Fix the symlinks in the repos pointing to libraries and to quiz and assignment definitions.
(`git config --local core.symlinks true` to keep them fixed).
* 201-016: Delete an unused problem.
* 201-016: Add a button that displays in the Library Browser
  that shows problems whose source code is in the template problem directory.

## 2024-01-13

* Create repo from the contents of the on-line model courses tracking only `course.conf`, `hide_directory`, and the contents of `templates/`.
* edit tips link in `course_info.txt` to point to the new docs location (this avoids a redirect).
* Create model201-SC1 from model201-103.
  - Just cosmetic (name) change
  - uses the 201-103 template assignments
* Create model201-SLA from model201-105.
  - Just cosmetic (name) change
  - uses the 201-105 template assignments
* Create model203-NYA-physics from modelChamplain2021.
  - Just cosmetic (name) change
* Create model203-NYB-physics from modelChamplain2021.
  - Just cosmetic (name) change
* Create model203-NYC-physics from modelChamplain2021.
  - Just cosmetic (name) change
