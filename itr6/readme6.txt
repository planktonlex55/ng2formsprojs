lets say we want to group elements.
eg. uname + uemail (input elements) and create a new ngmodelgroup "userData"

<div ngModelGroup="userData" #userData = "ngModelGroup">
  <!-- child component -->
</div>

u can use any name other than userData. 
Note:- ngModelGroup is only available in forms which use NgForm . 
               Read this shit: https://angular.io/api/forms/NgModelGroup 
               
Once u use this, userData becomes visible under form->controls->userData   


U can now do validations on all the elements in the group:
  <div *ngIf="userData.touched && !userData.valid ">
    <span class="help-block">Plz enter correct userData</span>
  </div>

