# ILIAS_test_stringcompare
Python script to check for duplicate answers in the test results of the online learning (and examination) platform ILIAS.

The learning platform ILIAS (https://www.ilias.de/lms-ilias-hochschulen/, https://ilias.uni-freiburg.de/ilias.php) 
offers to conduct online/remote exams via the _test_ feature.
Free text questions, where students can enter their own writing, are a crucial element of this type of exam, 
but prone to plagiarism if the exam is carried out remotely. 
This is because it is very easy to just copy-paste any text into the text fields, 
including sample answers that were circulated among students beforehand.

This script reads the xlsx export of all answers from an ILIAS test 
(for each participant, there is an own sheet with all answers)
and checks for each n(n-1)/2 pairs of students whether there are duplicate answers among ILIAS test results.

More specifically, for each question, the script creates a lower triangular matrix 
where the numerical value represents the longest common substring of the two answers given by the pair of students.
Unusually long substrings and thus overlapping answers can be easily spotted and manually checked further.
(It may turn out that students just copied part of the text of the task at hand, 
 or they actually copied their answer from another source but their own writing!)

This script is rather slow, so any improvement of its performance will be appreciated!
