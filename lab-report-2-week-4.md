# Bugs, Symptoms, and Failure-Inducing Inputs

## 1. Extra characters at end of file causing infinite loop

![Infinite loop bug fix](./2-1_loop-fix.png)

A link to the file containing the failure-inducing input that prompted this change can be found [here.](https://github.com/mwchen25/markdown-parser/edit/main/test-file.md)

The symptom of this failure-inducing input was an infinite loop, so there was no output after running the file at the command line until the loop was manually terminated.

The bug was that the code did not address how to handle additional characters at the end of the input file. Therefore, any file with additional characters after its final link such as the one above could be considered a failure-inducing input, and would trigger the symptom of an infinite loop.

## 2. Code not recognizing images

![Image detection bug fix](./2-2_image-detection.png)

A link to the file containing the failure-inducing input that prompted this change can be found [here.](https://github.com/mwchen25/markdown-parser/blob/main/test-file-3.md)

The symptom of this failure-inducing input was images being printed out alongside website links, when only website links were supposed to be printed.

The bug was that the code did not recognize when a link represented an image versus a website, so any file containing an image was a failure-inducing input. The symptom of this bug was the link to an image being printed, even though it should not have been printed.

## 3. Missing parentheses causing infinite loop

![Infinite loop bug fix](./2-3_loop-fix.png)

A link to the file containing the failure-inducing input that prompted this change can be found [here.](https://github.com/mwchen25/markdown-parser/blob/main/test-file-4.md)

The symptom of this failure-inducing input was the same as in the first bug: since it caused an infinite loop, there was no output after running the file at the command line until the loop was manually terminated.

The bug was that the code could not handle an input without parentheses, as it continuously checked for parentheses without a way to exit if they were not in the file. Therefore, any file without parentheses was a failure-inducing input that would have caused the symptom of an infinite loop.