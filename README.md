### Wordpres-search
This is aquick tutorial for all who needs to place a nice looking search form on your Wordpress Theme.

It will have a lens icon (Fontawesome) and Bootstrap styling.

Once you have installed Bootstrap and Fontawesome,  go to your theme root folder, create a **searchform.php** and paste this code.

```php
    <form role="search" method="get" class="form-inline my-2 my-lg-0" action="<?php echo esc_url( home_url( '/' ) ); ?>">
      <div class="input-group">
        <input type="search" class="form-control" placeholder="<?php echo esc_attr_x( 'Search &hellip;', 'placeholder', 'your-text-domain' ); ?>" value="<?php echo get_search_query(); ?>" name="s" title="<?php echo esc_attr_x( 'Search for:', 'label', 'your-text-domain' ); ?>">
        <div class="input-group-append">
          <button class="btn btn-secondary" type="submit">
            <i class="fas fa-search"></i>
          </button>
        </div>
      </div>
    </form>
```
    
Nou can display the form in your theme by calling **get_search_form();** in the appropriate template file. Example:

```php
<header>
	<div>
		//Some code...
	</div>
	<div class = "search" > 
		 <?php  get_search_form(); ?>
	</div>
</header>
```
