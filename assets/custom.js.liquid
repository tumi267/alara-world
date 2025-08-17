$(document).ready(function () {
    // First, check if the popup was already shown
    var popupShown = localStorage.getItem('popup_shown') === 'true';

    if (!popupShown) {
        // Delay showing the popup to avoid flickering
        setTimeout(function () {
            $('.global-newsletter-section').fadeIn(); // optional fade effect
            $('body').addClass('is-popup-active');
        }, 3000); // Show after 3 seconds
    }

    // Event listener for clicking outside of the popup
    $('body').on('click', function (event) {
        if (!$(event.target).closest('.global-newsletter-section').length) {
            $('.global-newsletter-section').hide();
            $('body').removeClass('is-popup-active');
            localStorage.setItem('popup_shown', 'true');
        }
    });

    // Event listener for clicking the close icon
    $('body').on('click', '.global-newsletter-section svg.icon.icon-close', function () {
        $('.global-newsletter-section').hide();
        $('body').removeClass('is-popup-active');
        localStorage.setItem('popup_shown', 'true');
    });
});


// pdp slider 
$('.product--thumbnail_slider button.slider-button.slider-button--next').on('click', function (e) {
    e.preventDefault();
  // Find the currently active thumbnail
  $(this).removeAttr('disabled');

  var $currentThumb = $('.thumbnail[aria-current="true"]');

  // Get its parent <li>, then the next <li> sibling
  var $nextLi = $currentThumb.closest('li').next('li');

  // If the next <li> exists, trigger a click on its .thumbnail child
  if ($nextLi.length > 0) {
    $nextLi.find('.thumbnail').trigger('click');
  }
});
$('.product--thumbnail_slider button.slider-button.slider-button--prev').on('click', function (e) {
   e.preventDefault();
  $(this).removeAttr('disabled');

  var $currentThumb = $('.thumbnail[aria-current="true"]');
  var $currentLi = $currentThumb.closest('li');
  var $prevLi = $currentLi.prev('li');

  if ($prevLi.length > 0) {
    $prevLi.find('.thumbnail').trigger('click');
  } else {
    // If no previous li, go to the last
    $('.product--thumbnail_slider li').last().find('.thumbnail').trigger('click');
  }
});

// scroll down indicator

$('body').on('click', '.scroll--down-indicator.content', function () {
  
 
  const nextSection = $(this).closest('.scroll-down').next('.scroll-down');
  if (nextSection.length) {
    $('html, body').animate({
      scrollTop: nextSection.offset().top
    }, 500, 'linear');
  }

});


$('body').on('click', '.mobile--drawer--search button.search-modal__close-button', function (e) {
    e.preventDefault();
    e.stopImmediatePropagation(); 
    $('input.search__input.field__input').val('');
   
});




function initSliderIfNeeded() {
  const isMobile = window.innerWidth < 768;
  const isMac = /Mac/i.test(navigator.platform);
  const scrollDelay = isMac ? 1000 : 600;
  const $slider = $('.slick-slider-wrapper');

  if ($('body').hasClass('slick-slider-active')) {
    if (!$slider.hasClass('slick-initialized')) {
      $slider.slick({
        infinite: false,
        slidesToShow: 1,
        slidesToScroll: 1,
        vertical: true,
        verticalSwiping: true,
        dots: true,
        arrows: false,
        speed: 700,
        cssEase: 'ease-in-out',
        customPaging: function (slider, i) {
          let number = (i + 1).toString().padStart(2, '0');
          return '<button>' + number + '</button>';
        }
      });

      $slider.on('beforeChange', function (event, slick, currentSlide) {
        $(slick.$slides.get(currentSlide)).addClass('fade-out').removeClass('fade-in');
      });

      $slider.on('afterChange', function (event, slick, currentSlide) {
        $(slick.$slides.get(currentSlide)).addClass('fade-in').removeClass('fade-out');
      });

      // ✅ Desktop scroll
      let scrollThrottle = false;
      $slider.on('wheel', function (e) {
        const deltaY = e.originalEvent.deltaY;

        const sliderTop = $slider.offset().top;
        const sliderBottom = sliderTop + $slider.outerHeight();
        const scrollTop = $(window).scrollTop();
        const windowHeight = $(window).height();

        const inFullView = scrollTop >= sliderTop && (scrollTop + windowHeight) <= sliderBottom;
        if (!inFullView) return;

        if (scrollThrottle || Math.abs(deltaY) < 30) return;

        scrollThrottle = true;
        setTimeout(() => scrollThrottle = false, scrollDelay);

        if (deltaY > 0) {
          $slider.slick('slickNext');
        } else {
          $slider.slick('slickPrev');
        }

        e.preventDefault();
      });

      // ✅ Mobile Touch Scroll Fix
      let touchStartY = 0;
      $slider.on('touchstart', function (e) {
        touchStartY = e.originalEvent.touches[0].clientY;
      });

      $slider.on('touchmove', function (e) {
        const touchY = e.originalEvent.touches[0].clientY;
        const deltaY = touchStartY - touchY;

        const sliderTop = $slider.offset().top;
        const sliderBottom = sliderTop + $slider.outerHeight();
        const scrollTop = $(window).scrollTop();
        const windowHeight = $(window).height();
        const inFullView = scrollTop >= sliderTop && (scrollTop + windowHeight) <= sliderBottom;

        if (!inFullView) return; // Let browser scroll until slider is fully visible

        if (Math.abs(deltaY) < 20) return;

        if (deltaY > 0) {
          $slider.slick('slickNext');
        } else {
          $slider.slick('slickPrev');
        }

        e.preventDefault(); // Block native scroll only when inside slider
      });

      // ✅ Mac keyboard navigation
      if (isMac) {
        document.addEventListener('keydown', function (e) {
          if (!$('body').hasClass('slick-slider-active')) return;

          const activeElement = document.activeElement;
          const isInputFocused = activeElement &&
            (activeElement.tagName === 'INPUT' ||
             activeElement.tagName === 'TEXTAREA' ||
             activeElement.isContentEditable);
          if (isInputFocused) return;

          const sliderTop = $slider.offset().top;
          const sliderBottom = sliderTop + $slider.outerHeight();
          const scrollTop = $(window).scrollTop();
          const windowHeight = $(window).height();
          const inFullView = scrollTop >= sliderTop && (scrollTop + windowHeight) <= sliderBottom;

          if (!inFullView) return;

          if (e.key === 'ArrowDown') {
            $slider.slick('slickNext');
            e.preventDefault();
          } else if (e.key === 'ArrowUp') {
            $slider.slick('slickPrev');
            e.preventDefault();
          }
        });
      }
    }
  }
}








// Scroll header logic (unchanged)
let lastY = 0;
$('.section-header').addClass('scrolling-up');

$(window).on('wheel', function (e) {
  if (e.originalEvent.deltaY < 0) {
    $('.section-header').addClass('scrolling-up');
  } else {
    $('.section-header').removeClass('scrolling-up');
  }
});

let touchStartY = 0;
$(window).on('touchstart', function (e) {
  touchStartY = e.originalEvent.touches[0].clientY;
});

$(window).on('touchmove', function (e) {
  let touchEndY = e.originalEvent.touches[0].clientY;
  if (touchEndY > touchStartY) {
    $('.section-header').addClass('scrolling-up');
  } else {
    $('.section-header').removeClass('scrolling-up');
  }
  touchStartY = touchEndY;
});

// Click handler for scroll indicator
$('body').on('click', '.scroll--down-indicator.content', function () {
  const slideIndex = parseInt($(this).parents('.shopify-section').attr('data-slick-index'), 10);
  $('.slick-slider-wrapper').slick('slickGoTo', slideIndex + 1);
});

let scrollThrottle = false;

// Run once on load and again on resize
$(document).ready(initSliderIfNeeded);
$(window).on('resize', initSliderIfNeeded);
// mobile serach
$('.mobile--drawer--search.search-modal__content.search-modal__content-bottom').addClass('hidden-important')
$('body').on('click', '.mobile--drawer--serach', function (e) {
    e.preventDefault();
    e.stopImmediatePropagation(); 
    $('.mobile--drawer--search.search-modal__content.search-modal__content-bottom').removeClass('hidden-important').show();
    $('.header__darwer__icon-close').removeClass('hidden-important').show();
});

$('body').on('click', '.header__darwer__icon-close', function (e) {
  setTimeout(function() {
    $('.mobile--drawer--search.search-modal__content.search-modal__content-bottom').addClass('hidden-important');
    $('.header__darwer__icon-close').addClass('hidden-important');
    }, 200);
});

