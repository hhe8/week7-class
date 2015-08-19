ruby has memorization?
true && nil gives the result of nil;
things are false if they are false or nil;
logical evaluation is short circuited.
x = x || 100; x => 100; this is a technical to initialize a variable with a default value;
movie = movie || "apollo 13";
the shortcut here is movie||="apollo 13"


rails console:
Movie.first(5);
Movie.all.limit(5).pluck(:title);
Movie.find([id1,id2]); can use an array of movie ids;
under models.yml; use (default value) to give default value;


my account -- corresponds to the show action
what about sign in ? is it one of the 7 resources?
authentication, the identification of a person.

sessions controller!
once signed in, we need to remeber who they are and create a cookie.

rails generate new controller !

flash hash use :notice keyword. we can use notice object to be shown next page.
flash hash is great for showing messages.

reset_session clears all the cookie session

validates :password, confirmation:true

before_ation :find_movie
def find_movie
  # ...@movie = Movie.fund_by(:id => params["id"])
end
use instance variable in the controller methods

use find_by(:id => params["id"]) gives nil if there is no such id
use find(params["id"]) raises exception when there is no such id

before_action :find_movie, only: [:show, update, :edit, :destroy] the before action only works for these 4 actions


belongs_to class_name? foreign key:

f = Flight.first
