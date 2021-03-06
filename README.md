# Prism.Validation

[<img src="https://ci.appveyor.com/api/projects/status/github/mfe-/Prism.Validation?branch=master&svg=true">](https://ci.appveyor.com/project/mfe-/prism-extensions)

The Prism.Validation goal is to share extensions for the [Prism](https://github.com/PrismLibrary) framework, acroos the .NET application model also known as [App models](https://en.wikipedia.org/wiki/.NET_Framework#App_models). Therefore the Prism.Validation is shipped as PCL.

##Install
[Install](https://www.nuget.org/packages/Prism.Validation/) with nuget ```Install-Package Prism.Validation```

##Use
1. Install Prism.Validation in your model project with nuget ```Install-Package Prism.Validation``` 
2. Create your model class and inherit from ```ValidatableBindableBase```.
3. Decorate your properties with DataAnnotations like ```[StringLength(2, ErrorMessage = "Max 2 digits")]```
4. Set Binding in XAML like ```<TextBox Text="{Binding Path=Name,Mode=TwoWay}" />``` 

##Validation
Model classes are a good example which can be used to share across different platforms. Also you may want to add some basic validations into the model with DataAnnotaions.

The Prism Core Libary doesn't provide a validation implementation (Related [Issue](https://github.com/PrismLibrary/Prism/issues/625) on Prism), so the Prism.Validation libary is filling this gap. The validation was taken over from the UWP [ValidatableBindableBase](https://github.com/PrismLibrary/Prism/tree/de7b03b5e015edcac595602512877b264a1345d1/Source/Windows10/Prism.Windows/Validation) with litte adjustments.

With the Prism.Validation you could share your model with DataAnnotaion between wpf, xamarin and uwp. 

##Contribute
Contribute if you want.