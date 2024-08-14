<View style="font-size: 15px">
  <Header value="Task:" size="6"/>
  <Text name="task1" value="In the presence of this x-ray, the indication, finding A (reference), and your own impression of the image. Please assess the quality of findings B on the right." size="small" />
 
  
    <View style="font-size: 20px">
  <Header value="Indication:" size="6"/>
  	<Text name="cap1" value="$q1" size="large"/>
  </View>
    <View style="display: flex;">

  <View>      
        <Style> .task-ontent {text-shadow } </Style>
    <View className="task-ontent">   
      <Header value="Findings A(reference):"  size="6"/>
             </View>

        <View style="display: grid; grid-template-columns: 100fr 1fr 1fr 1fr; column-gap: 1em; overflow: auto;">

        	<Text name="Findings A(reference)" value="$Findings" size="large"/>
        </View>
              </View>
 <View>      
        <Style> .task-content {text-shadow: 1px 1px red; } </Style>
    <View className="task-content">
    <Header value="Findings B:(Please assess quality)"  size="6"/>
       </View>
  <View style="display: grid; grid-template-columns: 100fr 1fr 1fr 1fr; column-gap: 1em ;overflow: auto;">
        	<Text name="Findings B" value="$Findings" size="large"/>
      </View>
   
    </View>
     
     </View>
   <Image name="image1" value="$image" width="80%" zoom="true" />       

  
  
  
  <Choices name="First_Choice" toName="Findings B" choice="single" 
             showInLine="true">
      <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="Is there any part of Findings B that you do not agree with? (Double click the labeled area to expand the the available options)"  size="8" />
</View>
    <Choice value="Yes"  />
    <Choice value="No" />
  </Choices>
    
    <View visibleWhen="choice-selected" whenTagName="First_Choice" whenChoiceValue="Yes">
    <Labels name="disagreement" toName="Findings B" choice="single" maxUsages="1">

      <View style="font-size: 20px">
  <Header value="Add disagreement" size="8"/>
   </View>
      <Label value="Disagreement 1"  background="red"/>
  </Labels>
         </View>

 
   
  <Choices name="reasons" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected" whenLabelValue="Disagreement 1"
          >
    
<View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 8px;}
         .htx-ranker-item { width: 80px; height: 50px;background: lightgoldenrodyellow;font-size: 10px; }
         .htx-ranker-bucket-title {font-size: 11px;}
</Style>
       <Header value="Why do you disagree with this passage?" size="6"/>
</View>

    <Choice value="Finding I do not agree is present"  />
    <Choice value="Incorrect location of finding" />
    <Choice value="Incorrect severity of finding" />
    <Choice value="Refers to view that is not present" />
    <Choice value="Refers to prior study that is not present" />

  </Choices>
  
    

  <Choices name="Error-type" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
           whenLabelValue="Disagreement 1">
    <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="The error is:" size="6" />
</View>

    <Choice value="Clinically significant"  />
    <Choice value="Clinically insignificant" />
  </Choices>

  
      <View visibleWhen="region-selected" whenLabelValue="Disagreement 1">
   <Text name="v3" value="Write what you would put in place of the selected passage:" />
    <TextArea name="answer2" toName="v3" rows="3" maxSubmissions="1" placeholder="Rewrite here" />     
  </View>
  
  
   <Choices name="Add" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
           whenLabelValue="Disagreement 1">
    <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="Do you want to add another diaggrement?" size="6" />
</View>

    <Choice value="Add diaggrement"  />
    <Choice value="No diaggrement" />
  </Choices>
 
  <View visibleWhen="choice-selected"
        whenTagName="Add" whenChoiceValue="Add diaggrement">
     <Labels name="disagreement2" toName="Findings B" choice="single" maxUsages="1" >
    <View style="font-size: 20px">
  <Header value="Add disagreement" size="8"/>
   </View>
    <Label value="Disagreement 2" background="green" />
    
  </Labels>
  </View>

 
   
  <Choices name="reasons2" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
            whenLabelValue="Disagreement 2">

<View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 8px;}
         .htx-ranker-item { width: 80px; height: 50px;background: lightgoldenrodyellow;font-size: 10px; }
         .htx-ranker-bucket-title {font-size: 11px;}
</Style>
       <Header value="Why do you disagree with this passage?" size="6"/>
</View>

    <Choice value="Finding I do not agree is present"  />
    <Choice value="Incorrect location of finding" />
    <Choice value="Incorrect severity of finding" />
    <Choice value="Refers to view that is not present" />
    <Choice value="Refers to prior study that is not present" />

  </Choices>
  
    

  <Choices name="Error-type2" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
           whenLabelValue="Disagreement 2" >
    <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="The error is:" size="6" />
</View>

    <Choice value="Clinically significant"  />
    <Choice value="Clinically insignificant" />
  </Choices>

  
      <View visibleWhen="region-selected" whenLabelValue="Disagreement 2">
   <Text name="v4" value="Write what you would put in place of the selected passage:" />
    <TextArea name="answer3" toName="v4" rows="3" maxSubmissions="1" placeholder="Rewrite here" />     
  </View>
  
  
   <Choices name="Add2" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
           whenLabelValue="Disagreement 2">
    <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="Do you want to add another disaggrement?" size="6" />
</View>

    <Choice value="Add disaggrement"  />
    <Choice value="No disaggrement" />
  </Choices>
 
  <View visibleWhen="choice-selected"
        whenTagName="Add2" whenChoiceValue="Add disaggrement">
  <Labels name="disagreement3" toName="Findings B" choice="single" maxUsages="1">
    <View style="font-size: 20px">
  <Header value="Add disagreement" size="8"/>
   </View>
    <Label value="Disagreement 3" background="blue" />
    
  </Labels>
  </View>
 
   
  <Choices name="reasons3" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected" whenLabelValue="Disagreement 3"
           >

<View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 8px;}
         .htx-ranker-item { width: 80px; height: 50px;background: lightgoldenrodyellow;font-size: 10px; }
         .htx-ranker-bucket-title {font-size: 11px;}
</Style>
       <Header value="Why do you disagree with this passage?" size="6"/>
</View>

    <Choice value="Finding I do not agree is present"  />
    <Choice value="Incorrect location of finding" />
    <Choice value="Incorrect severity of finding" />
    <Choice value="Refers to view that is not present" />
    <Choice value="Refers to prior study that is not present" />

  </Choices>
  
    

  <Choices name="Error-type3" toName="Findings B" choice="single" showInLine="true"
           visibleWhen="region-selected"
            whenLabelValue="Disagreement 3" >
    <View>
  <Style>.htx-ranker-column {width: 700px; height: 400px;font-size: 10px;}
         .htx-ranker-item { width: 270px; height: 50px;background: lightgoldenrodyellow;font-size: 14px; }
         .htx-ranker-bucket-title {font-size: 12px;}
</Style>
       <Header value="The error is:" size="6" />
</View>

    <Choice value="Clinically significant"  />
    <Choice value="Clinically insignificant" />
  </Choices>

  
      <View visibleWhen="region-selected"  whenLabelValue="Disagreement 3">
   <Text name="v5" value="Write what you would put in place of the selected passage:" />
    <TextArea name="answer4" toName="v5" rows="3" maxSubmissions="1" placeholder="Rewrite here" />     
  </View>

</View>