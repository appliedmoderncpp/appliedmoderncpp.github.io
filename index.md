# Summary

* [Course aims](#course-aims)
* [Student learning outcomes](#student-learning-outcomes)
* [Assumed knowledge](#assumed-knowledge)
* [Course staff](#course-staff)
* [Course details](#course-details)
* [Course resources](#course-resources)
* [Teaching rationale](#teaching-rationale)
* [Teaching strategies](#teaching-strategies)
* [Assessment](#assessment)
* [Academic honesty and plagiarism](#academic-honesty-and-plagiarism)
* [Course evaluation and development](#course-evaluation-and-development)

# Course aims

This course aims to introduce students to intermediate and advanced programming using modern C++. Students will learn about and use the core features of C++, while learning how to integrate them into well-designed programs.

## Content in a nutshell

* Week 1 begins by considering some introductory features, such as data types, sequence, selection, iteration, functions, and error handling, and how good-practice in C++ differs to other programming languages with similar syntax \(yes, there's a difference!\).

* Week 2 takes a sharp turn, completely diverging from the course textbook, and introduces the Standard Library. Here, we consider Standard input/output library, Standard containers, Standard algorithms, and Standard utilities. Some of the content is so new that it does not exist in any textbook. By the conclusion of Week 2, students shall be well-equipped to complete their assignment.

* Week 3 returns to the textbook, and aims to design a program in class. This week aims to be an open discussion with students, and its success is dependent on student input. The subsequent tutorial shall also be dependent on the design decisions made in this week's lecture.

* Week 4 introduces a GUI framework that we will use to explore class design and run-time polymorphism. We will discuss mutability, base classes, derived classes, overriding functions, interface inheritance, and implementation inheritance (and why it is bad). Students should be thoroughly prepared for this week, as we will be covering initial material very quickly, and won't be able to slow down until we're in the thick of the lecture.

* Week 5 continues our discussion on class design, focusing on Invocable objects (lambdas and functors), default arguments, GUI design, how callbacks play a role in GUI programming, and what happens when a class derives more than one base.

* Week 6 discusses the free store, pointers, and memory management. This is a hard diversion from previous years, which introduce pointers much earlier on in the course. In this week, we will consider concepts related to moving and copying objects that own resources.

* Week 7 builds upon Week 6 \(so don't miss Week 6!\), and considers the difficulties and problems with explicitly managing resources. We will learn about the central feature of C++ -- Resource Acquisition Is Initialisation \(RAII\) -- and how it reduces the burden of explicit resource handling. We will also take a look at Standard smart pointers, which further reduce this burden by almost completely eliminating explicit resource handling through the type system.

* Weeks 8 begins our introduction to template-based generic programming. We will already have started learning about generic programming along the way, but we shall now look at how we can manipulate types and values to allow for greater flexibility. We will also look at constraint-based -- or concept-based -- programming, which is a natural extension to templates.

* Week 9 discusses how to write a Standard-conforming container, and how to write a generic algorithm. This material considers how a library developer might write `std::list`, and how we'd write something very general, such as `inner_product`.

* Week 10 looks at iterators and sentinels, and how C++ programmers can use them to enhance generic programming patterns. We will take our `list` container from Week 9 and add both an iterator and a sentinel to complete the container. Both Weeks 9 and 10 are critical for completing the fourth assignment.

* Week 11 will be our revision week. We'll cover the philosophy, history, and ideals of C++ in the first part of the lecture: this will lay the groundwork for you to do exam revision. After we cover the ideals and history of C++, we'll blitz through the entire course, starting from the top, and working our way down to iterators and sentinels. By the end of this week, you should be well-equipped to study for the final exam, which should confirm that you have satisfied the outcomes for the course, as listed below.

* Week 12 is an optional week that considers the relationship between C and C++. We look at the sibling-like relationship between C and C++, and discuss how the two programming languages diverge, and what it means for your programming style. We especially consider why you shouldn't write C-like code when you have access to a C++ compiler. We'll also talk about calling C code in C++, and calling C++ code using C, and identical code that when compiled using a C compiler gives very different results to compiling with a C++ compiler. This week is not assessed in the exam.

## Standard C++ and Technical Specifications

As a student of _Applied Modern C++_ in 2017, you will learn about C++17, the Concepts Technical Specification, and the Ranges Technical Specification.

The International Organization for Standardization publishes a few different kinds of documents: two of which are International Standards and Technical Specifications.

An International Standard is the Law for a Standard: anyone that claims that they're Standard-compliant needs to follow this document to the letter. We will commonly refer to the International Standard for C++ as "the Standard", or simply "C++17".

A Technical Specification is like a beta version of a feature. It's thoroughly specified, and there's a huge calling for whatever is in that TS, but more research about how it is to be used is necessary before it can be put into the International Standard. This process usually takes three to six years for C++.

## Audience

Students wishing to learn about industrial programming techniques, low-latency programming, object-oriented programming, and generic programming are the intended audience for this course.

We use C++ as a tool, not as the focus for this course.

# Student learning outcomes

[Graduate attributes](http://teaching.unsw.edu.au/sites/default/files/upload-files/GradAttrEng.pdf) are the qualities, skills, and understanding that the faculty agrees that its students should develop during their studies. Some of these graduate attributes are developed and assessed in this course. We outline the expectations below.

## Knowledge outcomes

By the conclusion of this course, you can expect to understand:

* how to write programs using Standard C++,
* why C++ programmers practice programming idioms that may differ from other programming languages,
* how to model object-oriented programming using C++,
* how to model constraint-based generic programming using C++,
* when to rely on resource management and when to manage your own resources,
* how a C++ library author thinks,
* how to choose between different third-party libraries,
* how to write unit tests for testing,
* why it is important to measure performance before making claims,
* the CppCoreGuidelines, and
* how to make simple tasks simple!

## Skill outcomes

By the conclusion of this course, you can expect to be able to:

* read and comprehend existing C++ programs,
* write and maintain C++ programs,
* effectively employ core features of C++,
* write clear and easy-to-understand C++,
* utilise the following libraries:
  * C++ Standard Library,
  * Ranges TS,
  * Guideline Support Library,
  * a subset of range-v3,
  * a subset of the Boost Programming Libraries,
* write object-oriented code using C++ abstractions,
* write generic code using C++ abstractions,
* generalise types to concepts,
* write code that relies on resource management tools,
* write code that employs its own resource management,
* write code that measures performance,
* use gdb for debugging, and
* use profiling tools like AddressSanitizer and Valgrind

Some voluntary outcomes \(i.e. if you study the starter files for your assignments\):

* Learning about the CMake build system
* Learning about source control through git and GitHub
* Learning about continuous integration through TravisCI 

# Assumed knowledge

No prior knowledge is necessary.

## Motivation and workload

You should have a clear motivation for enrolling in this course. **It is expected that students spend fifteen to twenty hours or more per week studying for this course.** This _includes_ attending watching videos, reading, completing assigned exercises, and working on assignments.

If you are only taking this course because you think it will impress an employer, you should reconsider taking this class. Students lacking a genuine interest in problems that C++ is typically used to solve and students who do not put the necessary time into studying the course historically perform poorly.

Students wishing to learn more about where C++ is applied in industry, and what problems the language can solve should take a look at [Bjarne Stroustrup's list of applications](http://stroustrup.com/applications.html) written in C++.

Broadly speaking, C++ can be applied to the following domains:

* algorithm development,
* biomedical applications,
* compilers and compiler-related tools,
* defence systems,
* desktop environments \(e.g. KDE for Linux\),
* embedded systems,
* Facebook,
* financial programming \(e.g. IMC, Morgan Stanley\),
* Google,
* operating systems,
* photo-editing software \(e.g. Adobe Photoshop\),
* poker machines,
* servers,
* telephone software,
* video games,
* web browsers

A large number of these were taken directly from Bjarne's list for a quick lookup. Bjarne provides a much more comprehensive list on his own website.

# Course staff

| Staff | Role | Email
| :--- | :--- | :--- |
| Christopher Di Bella | Lecturer | applied.modern.cpp@gmail.com |

# Course resources

## Prescribed course textbooks

| Author | Title | Edition | ISBN |
| :--- | :--- | :--- | :--- |
| Bjarne Stroustrup | [Programming -- Principles  and Practice Using C++](http://www.stroustrup.com/programming.html) | Second | 978-0321-992789 |
| Bjarne Stroustrup | [A Tour of C++](http://www.stroustrup.com/Tour.html) | First | 978-0321958310 |

## Style guide

Assignments will be marked against the [CppCoreGuidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md). Lecture slides will often point you in the direction of reading the guidelines, but you should start reading them by the end of Week 2.

## References

We will occasionally refer to [cppreference.com](https://en.cppreference.com), which is a well-maintained C++ wiki. Some of the larger contributors to this reference are also key players in the evolution of C++, so they know what they are talking about.

If you are after a written reference, consider [_The C++ Programming Language (Fourth edition)_](http://www.stroustrup.com/4th.html) by Bjarne Stroustrup for a language reference, and [_The C++ Standard Library : A Tutorial and Reference_](https://www.bookdepository.com/C-Standard-Library-Nicolai-Josuttis/9780321623218) by Nicolai Josuttis for a reference on the Standard Library.

## Other texts on C++

Most C++ resources are utter garbage. If you wish to consult a different resource about C++, please make sure that it is on the peer-reviewed StackOverflow [_Definitive C++ Book Guide and List_](https://stackoverflow.com/questions/388242/the-definitive-c-book-guide-and-list), or is featured at a conference such as [CppCon](https://cppcon.org) or [C++Now](https://cppnow.org). Videos by [Jason Turner](https://www.youtube.com/user/lefticus1) and [Jon Kalb](https://www.youtube.com/channel/UCqxYMYaC0ucCMyhOMeKxd2Q) are also trustworthy. Becoming familiar with people that standardise C++ and following their blogs or works are also good once you're at an advanced level.

This might seem a bit elitist, but to paraphrase William Blackstone, it is far better that ten good resources on C++ are overlooked than one poorly-written resource lead you astray.

## Videos

There will sometimes be material that can be used to summarise topics, or offer insight into features. These videos will be given where they are relevant, and are prescribed.

## CppLang Slack

The C++ community has a Slack chatroom, where the community are more than happy to answer questions.
If you aren't happy with the lecturer's responses, or need an immediate answer, Slack is the place to go.

## Teaching rationale

This course can probably be completed in six-to-twelve months. A series of take-home assignments and a take-home exam are provided.

Programming is about using abstractions when they exist, and building appropriate abstractions when they do not. Above all, programming is about intention, and clearly communicating to both the computer and the next person that reads your code \(probably you\).

The course exposes you to existing abstractions through the Standard Library, Ranges TS, range-v3 library, and Boost Programming Libraries very early on. These libraries will expose you to a large variety of abstractions, and will prepare you for writing large-scale programs using C++.

The course spends a fair amount of time showing you how to build abstractions when none exist.

## Teaching strategies

The amount of effort that you put into this course will directly reflect how much you get out of it. When approached correctly, C++ can be very easy to learn. The problem is that most people take the wrong approach to learning C++. We aim to avoid this mistake in this course.

C++ has lots of rules that you will most likely never need to learn about, and we try to minimise exposing you to those facets of the language.

You should aim to watch all videos and complete all exercises.

The programming assignments are serious projects, and they become progressively more challenging as we cover more advanced topics. Failure to complete the exercises in the course textbook and class problem sets will make it very difficult for you to pass assignments, let alone the exam.

### Tutorials

Tutorials provide you with a chance to practice content learnt in lectures and set readings in a small and more personal environment. Your tutor will assist with solving problems. You should take advantage of tutorials by completing as much work ahead of the class, and then answering questions in the tutorial, and participating in tutorial discussions.

There are two sets of tutorial questions:

* **Class activity questions** will be marked.

* **Textbook questions** are supplied by your course textbook. Attempting these questions is an excellent way to master the content of the course.

## Assessment

The mark breakdown between the programming assignments and the final exam is

| Component | Marks |
| :--- | :--- |
| Assignments | 45 |
| Lab exam | 55 |
| Course evaluation | 2 \(bonus marks\) |

Your final mark will be calculated using the following algorithm:

```
final_mark = ranges::min(100, student.assignment + student.exam + student.bonus);
```

### Assignments

There will be four **individual** programming assignments, which are designed to challenge you to learn about programming with C++. Each assignment will be progressively more difficult than the previous assignment.

Lots of ground needs to be covered before reaching the more interesting programming assignments.

* Assignment 1 will require you to leverage the Standard Library and the Ranges TS. You will be expected to use these in tutorials and subsequent assignments, so it is imperative that you learn to use them very early on in the course.

* You will be asked to work on a problem that can be solved using object-oriented programming techniques and dynamic memory allocation in Assignment 2.

* Assignment 3 focuses on resource management using smart pointers.

* Assignment 4 is concerned with generic programming.

It is critical that you make a serious effort to complete these programming assignments. Exposure to these programming assignments will give you a head start for your exam study.

Discussion and problem solving with peers is encouraged, but you are not allowed to derive code together. Students should not send code fragments of assignments to each other in any form \(e.g. emails, listings, etc.\). Copying another's code, or purchasing code is considered serious academic misconduct, and is not permitted.

#### Testing and submission

Assignments will be downloaded and run on GitHub. You do not need any prior experience with Git, nor do you need any prior experience with GitHub, although you will need to [create an account](https://github.com). Please read this tutorial for [setting up your assignments](tutorials/git.md). This tutorial is unique for the course, so even if you are a Git veteran, please give it a read!

All testing will be performed using CMake, and you are encouraged to add your own tests. A minimal subset of tests will be provided to you for a dryrun, but these tests offer minimal coverage, and won't contribute to marks. Please read this tutorial for [adding tests to the test suite](tutorials/cmake.md).

**Warning: tests that you submit are still subject to the plagiarism policy. Students are known to collaborate by deriving tests together -- tests that you submit must be _your own_ work. Please read the plagiarism policy below.**

Upon submission, your tests will run on a Travis CI build machine, where it will sit until the lecturer approves marking. There is a `.travis.yml` source file in your assignment that enables building. Please do not modify this file. **Any modification to `.travis.yml` will result in a zero for your assignment.**

### Lab exam

There will be a **three-hour, closed-book laboratory exam** for this course in the November exam period. Some documentation will be provided, so it is recommended that you familiarise yourself with the documentation on [cppreference.com](https://en.cppreference.com) and the [CppCoreGuidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md) early on in the course for speedy lookups in the exam. Access to the Web is not permitted.

All material covered in this course, including lectures, tutorials, assignments, set readings, and problem sets are examinable.

You will be asked to solve a series of problems using C++, and will need access to both a compiler and documentation, which is why this is a lab exam. Exam marking will be broken into two parts:

Exam correctness is evaluated through auto-marking. Be sure to regularly submit your work, as any submissions made after the three-hour allotted time period will be ignored.

**The lab exam is a hurdle requirement: you must pass the final exam to pass the course.**

## Academic honesty and plagiarism

Plagiarism is defined as "using the words or ideas of others and presenting them as your own."

This course treats plagiarism as academic misconduct, which means that it carries penalties as severe as being excluded from further study at UNSW. There are several online sources to help you understand what plagiarism is, and how it is dealt with at UNSW.

* Learning Centre: [Academic integrity & plagiarism](http://www.lc.unsw.edu.au/academic-integrity-plagiarism)
* myUNSW: [plagiarism](https://student.unsw.edu.au/plagiarism) and [misconduct](https://student.unsw.edu.au/conduct)
* CSE: [Addendum to UNSW Plagiarism Guidelines](http://www.cse.unsw.edu.au/~chak/plagiarism/plagiarism.html)
* CSE: [Yellow Form](http://www.cse.unsw.edu.au/people/studentoffice/policies/yellowform.html)

Make sure that you read and understand these. Ignorance is not accepted as an excuse for plagiarism.

## Course evaluation and development

Student feedback on this course will be obtained via electronic survey at the end of semester, and will be used to make continual improvements to the course.

You are encouraged to provide informal feedback to throughout the semester, and to let the lecturer know of any problems as soon as they arise. All reasonable suggestions and concerns will be carefully considered, and every effort will be made to address them.

Due to the abysmal student participation in previous years, this year will feature a **non-anonymous survey worth two bonus marks**. These bonus marks can be used to prop you up. You may submit either the non-anonymous feedback, the anonymous feedback, or both \(preferable\). **No impact will be made to student marks if your non-anonymous review is less-than-pleasant: an honest scathing review is far more valuable than a calming review for two marks.**
