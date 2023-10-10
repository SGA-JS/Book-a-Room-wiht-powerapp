# Book-a-Room-wiht-powerapp




The title room name must be the exact same name as your meeting room mailbox that was created in your exchange.


I am using an existing Powerapp Template "Book a Room" and modify there.
![image](https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/5389aad4-c735-4b29-a452-dfd62e86b61d)



##Modification I had made

![image](https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/c3b94700-4b25-4f1c-a218-76737aa80b3b)

###1 at search object 
Default > First(Office365Users.SearchUser({searchTerm:User().Email}).Country).Country
this will filter your room list based on your country location.
<img width="628" alt="image" src="https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/c118c2b9-47a3-4823-8e14-2ebf2465e22a">


###2 to show the capcity of a room
![image](https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/866abe9b-4000-4418-bb0f-c3a485c89f9b)

 
  ###2.1 create a SharePoint name RoomList as follows
<img width="480" alt="image" src="https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/1c3d799d-1508-4f85-a296-ba85dce07b12">

###2.2 Add a new "text label" to the "RoomGallery"
> "Size-" & First(Filter(RoomList, Title = ThisItem.Name)).Capacity
![image](https://github.com/SGA-JS/Book-a-Room-with-PowerApp/assets/73696641/12b69627-62e4-4bf4-916a-604b37d06cc7)

###3 Popup box for booking confirmation



  
