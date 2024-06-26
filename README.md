# **DAMIOTF ABOUT ME WEBSITE**


![Preview](https://damiotf.fun/github_img/1.png)

### **Scrolling down** or **clicking** "⬇️" will take you to the second part of the page smoothly

this .js script causes it

```js

        // Scroll logic
        $(document).ready(function() {
            let isScrolling = false;
            let currentSection = 1;
            const sections = $('.section');

            $(window).on('wheel', function(event) {
                if (isScrolling) return;

                isScrolling = true;
                if (event.originalEvent.deltaY > 0 && currentSection < sections.length) {
                    currentSection++;
                } else if (event.originalEvent.deltaY < 0 && currentSection > 1) {
                    currentSection--;
                }

                $('html, body').animate({
                    scrollTop: $(sections[currentSection - 1]).offset().top
                }, 1000, function() {
                    isScrolling = false;
                });
            });
        });

        // Scroll Function
        function scrollToNextSection() {
            let isScrolling = false;
            let currentSection = 1;
            const sections = $('.section');

            if (isScrolling) return;

            isScrolling = true;
            currentSection++;
            $('html, body').animate({
                scrollTop: $(sections[currentSection - 1]).offset().top
            }, 1000, function() {
                isScrolling = false;
            });
        }

```
# **SECOND PART OF WEBSITE**

![Preview](https://damiotf.fun/github_img/2-crt.png)

### You can disable the "*CRT*" effect by checking this box

![Preview](https://damiotf.fun/github_img/no-crt.png)

### Once selected, the page should look like this:

![Preview](https://damiotf.fun/github_img/2-no-crt.png)

