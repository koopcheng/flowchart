# Issues/Bugs

Before submitting what you believe to be a new issue or bug, please study carefully the documentation for flowchart by typing `help flowchart`. If your problem is not addressed, please go ahead and submit a [new issue](https://github.com/IsaacDodd/flowchart/issues/new/).

When submitting a new ticket, type `flowchart debug info` to receive helpful copy-and-paste system information collected by the package that will aide in understanding the issue since some problems are specific to certain setups (and type `flowchart debug` for more options). Please include the exact warning you received, the conditions or commands you typed in in order to get to that message, and any other information that may be helpful. Submitting bugs actually helps all users of the *flowchart* package.

# Contributions

The flowchart package has the potential of being an extremely useful addition to Stata. Your help is greatly needed and would be greatly appreciated! Here is how to get started contributing to the flowchart package.

- **Tests**: Use the two example files in the Ancillary Files as tests of whether the code builds or not after each change.
- **Debug**: Use the command `flowchart debug on` at the start of code you want to test and use `flowchart debug off` after it. This produces a DebugLog.log in the present working directory. This can be used to visualize how flowchart parses text and turns it into TikZ code. It functions a lot like a parser and somewhat like a [LALR Parser](https://en.wikipedia.org/wiki/LALR_parser).
- **Deprecated/Untracked Files**: In the .gitignore, a filename with an underscore ('_') at the start of it is ignored. So, you can use this to deprecate any files that you don't want git to track. Also, most of the LaTeX-generated file extensions have been ignored so you can build LaTeX documents without worrying about git recognizing all of the files it automatically generates.

### What Needs to be Done
- **Cleaning & Efficiency**: Help is needed to produce clean, readable TikZ code that still compiles and builds the same test files properly.
- **New Features**: The project is very open to new ideas. Please study the present source code and go right ahead and send a pull request.
- **Documentation**: Any improvements to the .sthlp documentation would be greatly appreciated.
- **Join the Team**: Please consider joining the flowchart package team to be a contributer - to handle issues/bugs, feature requests, and pull request approvals. Your help would be greatly appreciated.

### Attribution
You will be given the proper attribution for any contributions you make to the flowchart package.

### Pull Requests

When sending a new pull request, please submit the following information (an 'abstract') to help speed up the process of reviewing and approving your changes:

**Abstract:**
- **Branch Name**: `feature-[featurename]` - The branch name should have a name that summarizes the feature to be added.	
- **New Subcommand Name**: `flowchart [subcommandname]` - An explanation for subcommands is below.
- **Summary**: Give a 3-4 sentence summary of what the contribution does. After that 
- **Novelty**: Describe what this feature adds to the overall flowchart package if it is not apparent in the summary.
- **Explanation**: After that feel free to give a lengthier, detailed explanation of the technical aspects of the contribution.
- **To Do**: These are tasks that the developer approving your feature addition to the flowchart package should do.
- **Contact Infromation**: Leave the best way to contact you in case there are problems.
- **Attachments**: Drag and drop any images, screenshots, or samples of output that can be included onto the pull request in GitHub that you can provide to speed up the process of verifying that the feature works when it is tested.

**Template:**
Here is a template for the abstract: 

	[Abstract]
	Branch Name: 
	New Subcommand Name: 
	Summary: 
	Novelty: 
	Explanation: 
	To Do: 
	Contact Infromation: 
	Attachments: 

Use your judgment on which sections should be left out. After you submit your request, you will be contacted if there is a problem, the changes will be reviewed, and attribution will be assigned to you for your effort.

### Subcommand Names
If your new feature requires a new subcommand name to be added, please choose a terse, convenient word and account for commas and any other redundant words. 

The initial syntax parsing is handled by Stata's 'syntax' command. So, the token for the subcommand is stored into macro `1'.


	if("`1'" == "" | "`1'" == "mysubcommandname" | "`1'" == "mysubcommandname," | "`1'" == "alternativename") {
	
		... \\ Your Code Here
		
	}

Your command would then be accessed via `flowchart mysubcommandname ...` with any additional words or options.
	
Beyoned the initial 'if' statement for the subcommand you can do anything necessary to get your new feature to work: you can use the `gettoken` command to parse the input or whatever you would like and what does not break the code.

Thank you!