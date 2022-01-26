# CloudFormation
## 概要
awsリソースのプロビジョニングサービス。   
通常、マネジメントコンソールやCLIを利用しなければならないところを  
CloudFormationでテンプレート化してしまえば、同じ構成を何度も利用することが可能となる。  

・テンプレート  
どのawsリソースをどのような設定で記述するかを記載したもの。  

・スタック   
テンプレートからプロビジョニングされるawsリソースの集合体、スタック単位での管理ができる。   
スタックを作成したり、更新したりすることで、複数のリソースをまとめて管理することができる。   

## CloudFormationのメリット

・マネジメントコンソールの操作にかかる手間を削減することができる。   
・インフラ構成をバージョン管理することができる。   

## CloudFormationの仕組み

・テンプレート、スタック、自動プロビジョニングを実施する。   
・作成したテンプレート、スタックはS3上に保存される。   

## CloudFormationの書き方

・JsonまたはYaml形式で記述する。  
・一般的にはYamlのほうが可読性に優れているとされている。   

## デザイナー

・テンプレートのデザインをやってみる。

![image](https://user-images.githubusercontent.com/18514297/116708936-29591c00-aa0b-11eb-9da6-4d53a02e32a0.png)
![image](https://user-images.githubusercontent.com/18514297/116709188-632a2280-aa0b-11eb-85e9-511dfe43e616.png)

・デザイナーが起動したら、画面下部にあるテンプレートをクリック。   

![image](https://user-images.githubusercontent.com/18514297/116709403-98cf0b80-aa0b-11eb-9226-99ea108ab7c1.png)

・VPCとEC2をドラッグ&ドロップする。

![image](https://user-images.githubusercontent.com/18514297/116710053-4a6e3c80-aa0c-11eb-8b2d-70d896d3fef6.png)

・VPCの名前を変更する
![image](https://user-images.githubusercontent.com/18514297/116710326-96b97c80-aa0c-11eb-9bec-b035a4ae2d2f.png)
