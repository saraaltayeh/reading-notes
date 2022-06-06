# Associations

## four types of associations

- The HasOne association
- The BelongsTo association
- The HasMany association
- The BelongsToMany association

## Creating the standard relationships

1. To create a One-To-One relationship, the hasOne and belongsTo associations are used together;
2. To create a One-To-Many relationship, the hasMany and belongsTo associations are used together;
3. To create a Many-To-Many relationship, two belongsToMany calls are used together.

## One-To-One relationships

- Goal
that we have two models, Foo and Bar. We want to setup a One-To-One relationship between them such that Bar gets a fooId column.

- Options
Various options can be passed as a second parameter of the association call.

1. onDelete
2. onUpdate

## One-To-Many relationships

- Goal
 we have the models Team and Player. We want to tell Sequelize that there is a One-To-Many relationship between them, meaning that one Team has many Players, while each Player belongs to a single Team.

- Options
The options to be applied in this case are the same from the One-To-One case.

## Many-To-Many relationships

- Goal
 For this example, we will consider the models Movie and Actor. One actor may have participated in many movies, and one movie had many actors involved with its production. The junction table that will keep track of the associations will be called ActorMovies, which will contain the foreign keys movieId and actorId.

- Options
Unlike One-To-One and One-To-Many relationships, the defaults for both ON UPDATE and ON DELETE are CASCADE for Many-To-Many relationships.

Belongs-To-Many creates a unique key on through model. This unique key name can be overridden using uniqueKey option. To prevent creating this unique key, use the unique: false option.

## Special methods/mixins added to instances

- Foo.hasOne(Bar)
- Foo.belongsTo(Bar)
- Foo.hasMany(Bar)
- Foo.belongsToMany(Bar, { through: Baz })
