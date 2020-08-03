# Bulma Gutenberg

## Useage

To use please @import the /index.scss file of this package into your SCSS after you have imported Bulma.

You will need to remove the Gutenberg styles from loading on the front-end by adding this to your functions.php file.

    add_action( 'wp_enqueue_scripts', function(){
        wp_dequeue_style( 'wp-block-library' );
        wp_dequeue_style( 'wp-block-library-theme' );
        wp_dequeue_style( 'wc-block-style' ); // Remove WooCommerce block CSS
    } , 100 );

Support for wide and full align blocks has been added too. If you want to activate that, please add this to your functions.php file.

    add_action( 'after_setup_theme', function() {
      add_theme_support( 'align-wide' );
    } );

## Develop

### Requirements

- Yarn

### Installation

To develop please run `yarn` to install required packages

### Stylelint

We are following a set of stylesheet formatting rules. Please run `yarn lint:styles` before pushing to the repository.
