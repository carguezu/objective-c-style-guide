# Objective-C style guide
=======================
Personal Objective-C style guide.

This style guide is under construction. Feel free to open a pull request. 

## Sources

[NYTimes Objective-C Style Guide](https://github.com/NYTimes/objective-c-style-guide)

[Agbo Objective-C Style Guide](http://www.cocoaosx.com/2013/10/09/objectivec-style-guide-guia-de-estilo-objectivec-agbo/)

[Ray Wenderlich Objective-C style guide](https://github.com/raywenderlich/objective-c-style-guide)

[Robots & Pencils Objective-C Style Guide](https://github.com/RobotsAndPencils/objective-c-style-guide)

[GitHub Objective-C Style Guide](https://github.com/github/objective-c-conventions)

[Apple Coding Guidelines for Cocoa](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)

## Language

English should be used.

## Code Organization

Use `#pragma mark -` to categorize methods in functional groupings and protocol/delegate implementations following this general structure.

```objc

	#pragma mark - Lifecycle
	
	- (instancetype)init {}
	- (void)dealloc {}
	- (void)viewDidLoad {}
	- (void)viewWillAppear:(BOOL)animated {}
	- (void)didReceiveMemoryWarning {}
		
	#pragma mark - Drawing
	- (void)drawRect:(CGRect) {}
	
	#pragma mark - Overriden Methods
	- (void)someOverriddenMethod {}
		
	#pragma mark - Custom Accessors
	
	- (void)setCustomProperty:(id)value {}
	- (id)customProperty {}
	
	#pragma mark - IBActions
	
	- (IBAction)submitData:(id)sender {}
	
	#pragma mark - Public
	
	- (void)publicMethod {}
	
	#pragma mark - Private
	
	- (void)privateMethod {}
	
	#pragma mark - Protocol conformance
	#pragma mark - UITextFieldDelegate
	#pragma mark - UITableViewDataSource
	#pragma mark - UITableViewDelegate
	#pragma mark - NSCopying
	
	- (id)copyWithZone:(NSZone *)zone {}
	
	#pragma mark - NSObject
	
	- (NSString *)description 
```


## Dot-Notation Syntax

Dot-notation should **always** be used for accessing and mutating properties. Bracket notation is preferred in all other instances.

For example:

	view.backgroundColor = [UIColor orangeColor];
	[UIApplication sharedApplication].delegate;
	
Not:

	[view setBackgroundColor:[UIColor orangeColor]];
	UIApplication.sharedApplication.delegate;
	
...


