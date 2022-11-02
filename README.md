##Explain 

```
class Main extends Model
{
    public function posts()
    {
        return $this->hasManyThrough(
            'RelatedModel',
            'ThrougthModel',
            'country_id', // Foreign key on througt table...
            'user_id', // Foreign key on related table...
            'id', // Local key on main table...
            'id' // Local key on througt table...
        );
    } 
}
```
