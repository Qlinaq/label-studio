<View style="font-size: 20px">
  <Header value="Task:" size="3"/>
  <Text name="task1" value="1. VIEW the chest x-ray, then carefully READ the indication and the findings provided below. " size="large" />
  <Text name="task2" value="2. RANK the findings based on their overall quality using your best clinical judgment." size="large" />
  <View>      
    <Style> .task-content { color: red; } </Style>
    <View className="task-content">
  <Text name="task3" value="3. DO NOT PRODUCE TIES. Please assign each finding to exactly one rank." size="large" />
  <Text name="task4" value="4. IGNORE passages referring to multiple views or to a prior study. Those should NOT influence your ranking." size="large" />
   </View>
  </View> 
  <Text name="task5" value="5. SCROLL DOWN if needed to be able to read all findings in their entirety." size="large" />
   
  <View style="display: grid; grid-template-columns: 5fr 10fr 1fr 3fr; column-gap: 1em">
    <Header value="Question:"  size="2"/>
  </View>
  <View style="font-size: 20px font-weight: bold">
  	<Text name="q1" value="$q1"/>
  </View>
    <Image name="image" value="$image" width="50%" zoom="true"/>

<View style="font-size: 15px">
  <List name="results" value="$items" title="Candidate Choices"/>
  <Ranker name="rank" toName="results" />
</View>
  
  <Header value="Reference Answer:" size="3"/>
  <View  style="font-size: 20px">
  	<Text name="r1" value="$r1"/>
  </View>
  <Header value="Verification:" size="3"/>
  <Text name="v1" value="Is the Reference Answer correct according to the medical image, caption and question?"/>
  <View style="font-size: 20px">
   <Choices name="choice" toName="v1" required="true">
    <Choice value="Correct"/>
    <Choice value="Incorrect" />
  </Choices>
  </View>
  <Text name="v2" value="Do you have any feedback for us to improve this task going forward?"/>
  <TextArea name="answer1" toName="v2" rows="3" maxSubmissions="1" placeholder="Optional feedback here"/>
<Video name="video" value="$video"/>
</View>