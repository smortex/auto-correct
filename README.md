# auto-correct

Automatically correct students exercices.

## Usage

### Exam preparation

Extract *auto-correct* in any directory, add your questions as individual files
in the `questions` directory, they will be presented in alphabetical order.

Any question for which an answer is to be checked should have a corresponding
script in the `checkers` directory.  When checking the answer of the question
`question/sample-1`, the `checkers/sample-1` script will be evaluated.  It
should return 0 is the answer is correct, 1 otherwise.

Ensure students will be allowed to write to the `answers` directory, a sticky
bit will probably have to be set on this directory.

### Testing students

Ask them to source the `exam` script:

```
. ~teacher-login/path/to/auto-correct/bin/exam
```

Before leaving, ask them to show you the output of the `grade(1)` script.
