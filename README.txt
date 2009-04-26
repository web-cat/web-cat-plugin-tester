Web-CAT Plug-In Tester
======================
Current version: 0.1 (4/26/2009)

SUMMARY
-------
This tool is a standalone Java Swing application that is intended to be used by
authors of Web-CAT grading plug-ins so that they can test their plug-ins under
similar conditions to that under which they will run on Web-CAT, without the
hassle of having to upload the plug-in, create an assignment, and go through
the Web-CAT submission process with test code.

USAGE
-----
This application is distributed as an executable JAR; double-click it to bring
up the main window.

The application expects a directory structure like the following:

  -- testing area/
   \__ submission/
   \__ Results/
   \__ ScriptData/
   \__ test.properties

Each of these is described below:

* testing area:  the root directory in which all of the inputs and outputs for
  the grading plug-ins are stored (except for the plug-ins themselves). This
  folder can be named anything.
  
* submission:  the directory that contains the expanded files that will be
  compiled and executed with the plug-ins (think: a student's submission). This
  is the directory that you will specify in the user interface; the other
  directories in this tree will be determined from it.
  
* Results:  contains the output of the grading plug-ins; if this directory does
  not exist it will be automatically created.
  
* ScriptData:  optional; used to contain external files that the grading script
  may need access to, such as instructor's reference test cases or library
  code.
  
* test.properties:  optional; this file can contain properties that will be
  copied into the grading.properties file at the beginning of the grading
  process
  
THE USER INTERFACE
------------------

Submission:
  the path to the directory that contains the submission files to be graded;
  see "submission" in the file hierarchy above
  
Plug-ins to run:
  one or more directories that each contain a grading plug-in to be run on the
  submission
  
Properties:
  one or more lines each containing a "key=value" pair that will be copied into
  the grading.properties file at the beginning of the grading process
  
Documentation:
  Displays information about the properties that are available to be passed
  into the grading process.
