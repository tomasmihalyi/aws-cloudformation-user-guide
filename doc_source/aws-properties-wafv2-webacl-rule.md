# AWS::WAFv2::WebACL Rule<a name="aws-properties-wafv2-webacl-rule"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A single rule, which you can use in a WebACL or RuleGroup to identify web requests that you want to allow, block, or count\. Each rule includes one top\-level Statement that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\. 

## Syntax<a name="aws-properties-wafv2-webacl-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-rule-syntax.json"></a>

```
{
  "[Action](#cfn-wafv2-webacl-rule-action)" : [RuleAction](aws-properties-wafv2-webacl-ruleaction.md),
  "[Name](#cfn-wafv2-webacl-rule-name)" : String,
  "[OverrideAction](#cfn-wafv2-webacl-rule-overrideaction)" : [OverrideAction](aws-properties-wafv2-webacl-overrideaction.md),
  "[Priority](#cfn-wafv2-webacl-rule-priority)" : Integer,
  "[Statement](#cfn-wafv2-webacl-rule-statement)" : [StatementOne](aws-properties-wafv2-webacl-statementone.md),
  "[VisibilityConfig](#cfn-wafv2-webacl-rule-visibilityconfig)" : [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)
}
```

### YAML<a name="aws-properties-wafv2-webacl-rule-syntax.yaml"></a>

```
  [Action](#cfn-wafv2-webacl-rule-action): 
    [RuleAction](aws-properties-wafv2-webacl-ruleaction.md)
  [Name](#cfn-wafv2-webacl-rule-name): String
  [OverrideAction](#cfn-wafv2-webacl-rule-overrideaction): 
    [OverrideAction](aws-properties-wafv2-webacl-overrideaction.md)
  [Priority](#cfn-wafv2-webacl-rule-priority): Integer
  [Statement](#cfn-wafv2-webacl-rule-statement): 
    [StatementOne](aws-properties-wafv2-webacl-statementone.md)
  [VisibilityConfig](#cfn-wafv2-webacl-rule-visibilityconfig): 
    [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)
```

## Properties<a name="aws-properties-wafv2-webacl-rule-properties"></a>

`Action`  <a name="cfn-wafv2-webacl-rule-action"></a>
The action that AWS WAF should take on a web request when it matches the rule's statement\. Settings at the web ACL level can override the rule action setting\.   
*Required*: No  
*Type*: [RuleAction](aws-properties-wafv2-webacl-ruleaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-webacl-rule-name"></a>
A friendly name of the rule\. You can't change the name of a `Rule` after you create it\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OverrideAction`  <a name="cfn-wafv2-webacl-rule-overrideaction"></a>
The action to use to override the rule's `Action` setting\. You can use no override action, in which case the rule action is in effect, or count action, in which case, if the rule matches a web request, it only counts the match\.  
*Required*: No  
*Type*: [OverrideAction](aws-properties-wafv2-webacl-overrideaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-wafv2-webacl-rule-priority"></a>
If you define more than one `Rule` in a `WebACL`, AWS WAF evaluates each request against the `Rules` in order based on the value of `Priority`\. AWS WAF processes rules with lower priority first\. The priorities don't need to be consecutive, but they must all be different\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statement`  <a name="cfn-wafv2-webacl-rule-statement"></a>
The AWS WAF processing statement for the rule, for example ByteMatchStatement or SizeConstraintStatement\.   
*Required*: No  
*Type*: [StatementOne](aws-properties-wafv2-webacl-statementone.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityConfig`  <a name="cfn-wafv2-webacl-rule-visibilityconfig"></a>
Defines and enables Amazon CloudWatch metrics and web request sample collection\.   
*Required*: No  
*Type*: [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
