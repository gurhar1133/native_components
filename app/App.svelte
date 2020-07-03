<script>
    import { Template } from 'svelte-native/components';
    import { onMount } from 'svelte';
    import Button from "./Button.svelte";
    
    let message = "Svelte-Native Components Practice!";
    let label;
    let instructions = [
        {name: "1) Make components"},
        {name: "2) Refer to Veutify for the components design"},
        {name: "3) For this project (but not the web version), it is ok to alter App.svelte if you need to, just dont alter component calls "},
        {name: "4) See repo for instructions for icons"},
        {name: "5) Use tailwind, or vanilla css, whatever works"},
        {name: "6) Tabstrip instructions: Visit this link \nhttps://icons8.com/articles/ui-inspiration-tab-bar-animations/ \n to get inspiration to customize the tabstrip as you like (dont have to obsess over super fancy animation. Something nice and simple will suffice). Hint: rather than updating the current tabDtrip you may want to use gridLayout and to fix an element to the bottom of the screen"},
        {name: "7) Contact me with any issues"}
    ];

    let overlay1 = false;
    let overlay2 = false;

    $: gridItems = [
      {
        type: "Card", props: {
          title: "Card Test", 
          subtitle: "Test", 
          description: "Lorem ipsum blah blah blah",
          hasImage: true,
          imgSrc: "https://www.pngkey.com/png/detail/767-7671067_minecraft-pixel-art-grid.png",
          shaped: true
         
        }
        
      },
      {
        type: "Card", props:{
          title: "Card Test2", 
          subtitle: "Test", 
          description: "Lorem ipsum blah blah blah",
          hasImage: true,
          imgSrc: "https://www.lysergic.net/wp-content/uploads/2017/07/figure_grid_dimple_dylan_bakker-750x1000.jpg",
          shaped: true
         }
        
      },
      {
        type: "Card", 
        props: {
          title: "Card Test3", 
          subtitle: "Test", 
          description: "Lorem ipsum blah blah blah",
          hasImage: true,
          imgSrc: "https://images.artistrunwebsite.com/arwblog/bg_37311453262250.jpg?1453262251",
          shaped: true
        }
        
      },
      {
        markup: "<h3 class='text-xl' style='color:red;'>Hello World</h3>"
      },
      {
        type: "Button",
        props: {
          btnText: "Click me!",
          elevation: "lg",
          rounded: true,
          textMode: true
        }
        
      }
      
    ];
    
</script>

<style>
   
    
  
  
  
    
</style>


<page>
  
    <actionBar title="{message}" class="text-center bg-green-500 text-white px-2 py-4"/>
    <tabs iOSTabBarItemsAlignment="centerSelected" tabsPosition="bottom">
        <tabStrip highlightColor="#fff" selectedItemColor="#fff" class="bg-green-500 text-white" >
						<tabStripItem title="instructions">
                            <image src="font://&#xf015;" class="fas t-36" />
                        </tabStripItem>
						<tabStripItem title="Your components">
                            <image src="font://&#xf085;" class="fas fa-cogs" />
						</tabStripItem>
						
	    </tabStrip>

        <tabContentItem>
            <stackLayout  class="relative">
                <label text="Instructions" class="text-center text-xl bg-green-500 text-white py-2 px-2" />
                    <listView class="h-full"  items="{instructions}" >
								<Template let:item>
									<label class="text-center" text="{item.name}" textWrap="true" />
								</Template>
			        </listView>
            </stackLayout>
        </tabContentItem>

        <tabContentItem>
       
        <scrollView>
        <stackLayout>
        
            <label text="Buttons" class="text-center text-xl bg-green-500 text-white  py-2 px-2 m-b-4" />
               
                    <!--
                        Buttons go here
                    -->
                    
                <!-- <Button 
                    
                    btnText="Large Primary"
                    color="primary"
                    size="xl"
                    elevation="sm"
                    on:tap={()=>{
                        console.log("tap tap");
                    }}
                />  -->

            <!-- Buttons can have different levels of elevation -->

                <!-- <Button 
                   
                    btnText="Block Secondary Raised High"
                    color="secondary"
                    size="block"
                    elevation="lg"
                /> -->

                <!--default color should be purple like vuetify buttons
                        default size is md-->

                <!-- <Button
                    
                    btnText="Rounded"
                    size="lg"
                    rounded={true} />  

                <Button 
                    
                    btnText="Outline"
                    outline={true}
                    elevation={"none"} />

                    <Button 
                       
                        btnText="Outline"
                        outline={true}
                        elevation={"none"}
                        color="primary" />

                <Button 
                    
                    btnText="Text Button"
                    textMode={true} 
                    elevation={"none"}/>  -->

            <!-- by default disabled is false. Buttons should be disableable-->
 
                <!-- <Button
                    
                    btnText="Disabled"
                    disabled={true} /> -->

                <!-- put font awesome comment icon in this button. No btnText-->

                <!-- <Button fab={true} 
                        elevation="lg"
                        iconString="f075"/>

                <Button fab={true} 
                        elevation="sm"
                        size="lg"
                        iconString="f075"/> -->
                    
                   
            <label text="Cards" class="text-center text-xl bg-green-500 text-white  py-2 px-2 my-4"  />
                <!--
                        Cards go here
                -->
                <!-- <Card title="Vegeta"
                        platform="{platform}"
                        subtitle="Prince of Sayans"
                        description="Lorem ipsum ....."
                        hasImage={true}
                        imgSrc="https://i.redd.it/1xlrjb24x4f41.jpg"
                        elevation="lg"
                    >
        
                    </Card> -->

                <!-- <Card title="Svelte"
                        platform="{platform}"
                        subtitle="Javascript Framework"
                        description="Lorem ipsum ....."
                        hasImage={true}
                        imgSrc="https://i0.wp.com/programmingwithmosh.com/wp-content/uploads/2019/12/1_OJLglSTFZ1PbwpRG0U2xXA.png?ssl=1"
                        elevation="sm"
                    >
        
                    </Card> -->

                <!-- nesting Button in Card -->

                <!-- <Card title="Card with buttons"
                            platform="{platform}"
                         subtitle="No Image"
                        >

                        <Button fab={true} 
                            elevation="lg"
                            iconData={comment}/>

                    </Card> -->
 
 
                    <!-- <Card title="Tailwind"
                            platform="{platform}"
                            subtitle="Design"
                            description="Lorem ipsum ....."
                            hasImage={true}
                            shaped={true}
                            imgSrc="https://pbs.twimg.com/profile_images/895274026783866881/E1G1nNb0.jpg"
                            elevation="lg"
                    >
        
                    </Card> -->


                <!-- Come up with your own bonus card attribute for this one.
                Doesnt have to fit the vuetify design pattern. Could be animation, styling, etc-->  

                    <!-- <Card title="Bonus"
                                platform="{platform}"
                                subtitle="Your own bonus property"
                                description="Lorem ipsum ....."
                                hasImage={true}
                                shaped={true}
                                imgSrc="https://www.travelweek.ca/wp-content/uploads/2020/04/Travel-Edge-investing-50-million-in-signing-bonus-incentive-for-luxury-travel-advisors.jpg"
                                bonus={true}
                                >
        
                            </Card> -->
            
           <label text="Overlays" class="text-center text-xl bg-green-500 text-white  py-2 px-2 m-b-4" />
                <stackLayout class="h-64 w-full bg-green-200">
                    <!-- <Button 
                            platform="{platform}"
                            btnText="Show Overlay"
                            color="primary"
                            size="xl"
                            elevation="sm"
                            on:tap={()=>{overlay1 = !overlay1}}
                            /> 


                    <Overlay absolute="{true}" 
                            platform="{platform}"
                            opacity="{.5}" 
                            zIndex="{99}" 
                            value="{overlay1}" 
                        > 
                            <Button 
                            platform="{platform}"
                            btnText="Hide Overlay"
                            color="primary"
                            size="xl"
                            elevation="sm"
                            on:tap={()=>{overlay1 = !overlay1}}
                            />  


                            </Overlay>
                        
                        -->
                
                </stackLayout>
                


                        <!-- <Button 
                            platform="{platform}"
                            btnText="Show overlay"
                            color="primary"
                            size="xl"
                            elevation="sm"
                            on:tap={()=>{overlay2 = !overlay2}}
                        /> 
 

                <Overlay absolute="{false}" 
                        platform="{platform}"
                        opacity="{.2}" 
                        zIndex="{99}" 
                    value="{overlay2}"
                     >

      
        
                <Button 
                    platform="{platform}"
                    btnText="Hide Overlay"
                    color="primary"
                    size="xl"
                    elevation="sm"
                    on:tap={()=>{overlay2 = !overlay2}}
                /> 

            </Overlay> -->

            <label text="Textfields" class="text-center text-xl bg-green-500 text-white  py-2 px-2 m-b-4" />
                <!-- A see Vuetify examples for this basic text input -->

                <!-- <Textfield platform="{platform}" placeHolder="Default text input" />
                <Textfield platform="{platform}" placeHolder="Filled" filled={true} />
                <Textfield platform="{platform}" placeHolder="Oulined" outlined={true} /> -->

            <label text="Grids" class="text-center text-xl bg-green-500 text-white  py-2 px-2 m-b-4" />
             <!-- This builds on the gridLayout component -->
             <label text="Default two column" class="text-center bg-green-500 text-white  py-2 px-2 m-b-4" />
            
                <!-- <Grid gridElements={gridItems} /> -->

            <label text="One column" class="text-center bg-green-500 text-white  py-2 px-2 m-b-4" />
            
                <!-- <Grid gridElements={gridItems} numCols={1}/> -->

            <label text="Three column" class="text-center bg-green-500 text-white  py-2 px-2 m-b-4" />
            

                <!-- <Grid gridElements={gridItems} numCols={3}/> -->
        
        </stackLayout>
        </scrollView>
        
        </tabContentItem>

    </tabs>

</page>
