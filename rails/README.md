There are two different ways to do many-to-many relationships in Rails. The first is to use has_and_belongs_to_many, and the second is to use has_many with the through attribute.

However, it seems that has_and_belongs_to_many is no longer recommended and might be deprecated in the future. Based on this, it's probably safe to just use has_many.

First, we need two models where a many-to-many relationship makes sense. Users that can belongs to many groups works well.

    rails generate model user
    rails generate model group `

We will also need a model that represents the relationship between a user and a group, such as membership. Two attributes for representing a user and group are also added.

    rails generate model membership user_id:integer group_id:integer `

After doing this we still need to migrate for the database changes to take effect.

    rake db:migrate `

Lastly, we need to edit the model files user.rb and group.rb. The user model file should look like the following.

    class User < ActiveRecord::Base
        has_many :memberships
        has_many :groups, :through => :memberships
    end

And the group model should look like the following.

    class Group < ActiveRecord::Base
        has_many :memberships
        has_many :users, :through => :memberships
    end

So now the membership model will act as a join table between users and groups!

Source: http://railscasts.com/episodes/47-two-many-to-many
