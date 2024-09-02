(function($) {
  /**
   * Adds CSS styles to the document head.
   * @param {string} stylesString - The CSS styles as a string.
   * @returns {jQuery} The jQuery object for chaining.
   */
  $.fn.addStylesToHead = function(stylesString) {
    return this.each(function() {
        if (stylesString) {
            // Create a Blob with the styles
            const blob = new Blob([stylesString], { type: 'text/css' });
  
            // Generate an object URL for the Blob
            const url = URL.createObjectURL(blob);
  
            // Create a <link> element and append it to the document head
            const link = $('<link>', {
                rel: 'stylesheet',
                type: 'text/css',
                href: url
            });
  
            $('head').append(link);
        } else {
            console.warn('No styles content provided.');
        }
    });
  };
})(jQuery);
