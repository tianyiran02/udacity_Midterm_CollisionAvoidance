# Assignment Explain

## MP.1
The ring buffer created make use of std::deque. Image was push to the queue before the queue length was checked. If the length exceeding ring buffer length, then the front of the queue was removed.

## MP.2
This was done easily. Some worth mention:

1. OpenCV need to compile with extra coponents, so algorithms required in the assignment can be used.
2. FAST is not create with cv::FAST... No idea why the difference yet.

## MP.3
Pretty straight forward.

## MP.4, 5 and 6
Still, straight forwad. All algorithms use default parameters though.

## MP 7, 8 and 9
Please check the `AlgorithmComparison.xlsx` for detail comparison. Most important finding including:

- FAST detector is really fast... Gives plenty of result, I guess its also quite effort to find the most valuable result...
- BRIEF descriptor provides almost the same result as BRISK with 1/3 of processing time
- ORB detector is slow... But the result seems reliable. Extractor mathing rate are quite good
- AKAZA descriptor only works with AKAZA detector?

As for benchmarking, if only considering time, for AKAZA detector, result as follow. The matching results are similar...

FASTEST

- BRIEF
- BRISK
- ORB
- SIFT
- FREAK
- AKAZA

SLOWEST

For detector, it seems more tricky to compare since they generate different number of key points. Personlly I'll rank my preferece as below:

- BRISK
- AKAZA
- SIFT