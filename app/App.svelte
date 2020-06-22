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

                <!-- put an icon in this button. No btnText-->

                <!-- <Button fab={true} 
                        elevation="lg"
                        iconData={comment}/> -->

                <!-- <Button fab={true} 
                        elevation="sm"
                        size="lg"
                        iconData={comment}/> -->
                    
                   
            <label text="Cards" class="text-center text-xl bg-green-500 text-white  py-2 px-2 my-4"  />
                <!--
                        Cards go here
                -->
                <!-- <Card title="Vegeta"
                        subtitle="Prince of Sayans"
                        description="Lorem ipsum ....."
                        hasImage={true}
                        imgSrc="https://qph.fs.quoracdn.net/main-qimg-40ccab97c4b182082c3525bb34575a37.webp"
                        elevation="lg"
                    >
        
                    </Card> -->

                <!-- <Card title="Svelte"
                        subtitle="Javascript Framework"
                        description="Lorem ipsum ....."
                        hasImage={true}
                        imgSrc="https://i0.wp.com/programmingwithmosh.com/wp-content/uploads/2019/12/1_OJLglSTFZ1PbwpRG0U2xXA.png?ssl=1"
                        elevation="sm"
                    >
        
                    </Card> -->

                <!-- nesting Button in Card -->

                <!-- <Card title="Card with buttons"
                         subtitle="No Image"
                        >

                        <Button fab={true} 
                            elevation="lg"
                            iconData={comment}/>

                    </Card> -->
 
 
                    <!-- <Card title="Tailwind"
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
                            btnText="Show Overlay"
                            color="primary"
                            size="xl"
                            elevation="sm"
                            on:tap={()=>{overlay1 = !overlay1}}
                            /> 


                    <Overlay absolute="{true}" 
                            opacity="{.5}" 
                            zIndex="{99}" 
                            value="{overlay1}" 
                        > 
                            <Button 
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
                            btnText="Show overlay"
                            color="primary"
                            size="xl"
                            elevation="sm"
                            on:tap={()=>{overlay2 = !overlay2}}
                        /> 
 

                <Overlay absolute="{false}" 
                        opacity="{.2}" 
                        zIndex="{99}" 
                    value="{overlay2}"
                     >

      
        
                <Button 
                    btnText="Hide Overlay"
                    color="primary"
                    size="xl"
                    elevation="sm"
                    on:tap={()=>{overlay2 = !overlay2}}
                /> 

            </Overlay> -->

            <label text="Textfields" class="text-center text-xl bg-green-500 text-white  py-2 px-2 m-b-4" />
                <!-- A see Vuetify examples for this basic text input -->

                <!-- <Textfield placeHolder="Default text input" />
                <Textfield placeHolder="Filled" filled={true} />
                <Textfield placeHolder="Oulined" outlined={true} /> -->
        
        </stackLayout>
        </scrollView>
        </tabContentItem>

    </tabs>

</page>

<script>
    import { Template } from 'svelte-native/components';
    import Button from "./Button.svelte";
    let message = "Svelte-Native Components Practice!";
    let label;
    let instructions = [
        {name: "1) Make components"},
        {name: "2) Refer to Veutify for the components design"},
        {name: "3) Other than the tabstrip and uncommenting/importing components, dont alter App.svelte. "},
        {name: "4) See repo for instructions for icons"},
        {name: "5) Use tailwind, see repo for instructions"},
        {name: "6) Tabstrip instructions: Visit this link \nhttps://icons8.com/articles/ui-inspiration-tab-bar-animations/ \n to get inspiration to customize the tabstrip as you like (dont have to obsess over super fancy animation. Something nice and simple will suffice)."},
        {name: "7) Contact me with any issues"}
    ];

    let overlay1 = false;
    let overlay2 = false;
    
</script>

<style>
   
    
  
  
  
    
</style>

