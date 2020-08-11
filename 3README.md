
Title And Authors ;

Investigating Severity Thresholds for Test Smells

“Conference MSR-2020 Program”

Authors Name:-

(1) Davide Spadini

(2) Martin Schvarcbacher

(3) Ana-Maria Oprescu

(4) Magiel Bruntink

(5) Alberto Bacchelli

Introduction And Motivation:- 

Violations of design principles code smells) are not restricted to production code, but are also found in unit test code. Developers tend to focus on production code quality, while test code quality is often not prioritized; moreover, once test smells are introduced, they are hardly ever removed through refactoring. One could argue that the concept of test code quality and test smells in particular is in need of further investigation. For example, previous research has reported that developers do not always perceive test smells as problematic. Subsequently, we move to our second goal: We integrate test smell detection provided by tsDetect into a prototype (back-end) extension of BetterCodeHub 1 (BCH), a web-based code quality analysis tool provided by SIG. Calibrate detection thresholds such that severity levels can be assigned to a test smell instance, allowing developers to focus on the higher severity smells.  Improve the accessibility of automatic test smell detection by integrating into existing developer tooling.

(1) Calibrated severity thresholds for test smell detectors.

(2) A mechanism for rating the severity of certain test smells, allowing tools to classify test smells into distinct categories based on their severity. This enables developers to only focus on the most critical test smells. 

(3) An integration of an automatic test smell detector within a GitHub-based code quality tool (BCH). (4) An evaluation of developers’ perceptions of test smells within their own code bases, by integrating our new thresholds into a GitHub-based code quality tool (BCH), thus validating our test smell severity levels.

Research Methodology:- 

Research Q1= How can test smells be given a severity rating? 

Research Q2= What is the perception of developers on test smells in their codebase? 

Our overall research goal is to investigate severity thresholds for test smells. The most common test smell detection tools work on a binary scale of whether a given code is impacted by a test smell or not without any additional data, thus ignoring commonly encountered situations in software development. In our first research question, we seek to define new thresholds for test smells, based on the benchmark based threshold derivation methodology considering a large number of software systems.
Result:- 

Ans RQ1= We analyzed a corpus of 1,489 projects to determine the severity thresholds for 9 test smells (Empty Test and Ignore Test are excluded from this calibration since they are binary by default). The calibration results. Assertion Roulette has medium, high and very high severity set to 3, 5 and 10 respectively. These numbers represent the metric value in the case of Assertion Roulette, it represents the number of assertions without descriptions. This means that if a method has a test smell value below 3, it should be considered not smelly (or in other words, it belongs to the best 70% of the corpus); if it has a test smell value between 5 and 10 it should be considered as high severity (it belongs to the worst 20% methods of the corpus); above a value of 10 it should be considered as very high severity, since it belongs to the worst 10% of the corpus. As a first step to understand the test smells diffusion in open source projects using the new derived thresholds, we re-run the test smell analysis on our corpus of 1,489 projects using the new aforementioned thresholds. In Figure 3 we present the result. Since out of the scope of this paper, we did not further investigate the test smells diffusion on OSS systems.

Ans RQ2= In this RQ, we want to investigate developers’ overall perception on test smells found in their codebase: to this aim, we asked them to indicate for each test smell instance whether they would classify it as a valid instance to remove, how much priority they would give to the refactoring, and how long it would take according to them. We got a total of 301 responses. In Table 7 we show the impact ratings for test smell instances which were rated as either short or long term refactoring candidates (no action excluded). Smell evaluation. We now discuss the finding for each test smell separately, taking into account the optional additional remarks field (SQ4) of the survey, where the user could add remarks regarding their perception of the smell.

Conclusion:-

In this paper, we investigated the classification of test smells based on their severity. To do this, we define metrics for each test smell and then apply the benchmark-based threshold derivation on a sample of open-source projects. The result of this process allows us to give test smells a severity rating, from low to very high, which we verified with a sample of developers using their test source code to see if they agree with the rating classification. For four test smells (Assertion Roulette, Eager Test, Verbose Test and Conditional Test Logic), we defined non-binary severity thresholds and have a statistically significant difference between our proposed severity and user-perceived maintainability impact. Furthermore, Verbose Test and Conditional Test Logic showed a high statistically significant relationship and a strong Spearman coefficient.
Furthermore, we analyzed test smells the developers marked as won’t fix, trying to discover the reasons behind it, indicating how test smell detection tools could be improved to match the developer’s views on what is a test smell. This information can also be used to enhance the proposed test smell severity ratings. Furthermore, we have shown that test smell detection can be successfully integrated into a code quality tool to inform developers on test issues and help make tests more maintainable.

