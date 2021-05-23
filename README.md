# Must have Sass mixins usage

personal collection of usefull SASS mixins

## Reset List Elements

    ul {
        @include resetList(); // display:block default
    }

## Round Corners

    .round {
        @include roundedCorners(10px); // 5px default
    }

## Shadow

    .element {
        @include shadow([settings]);
    }

## Background Gradient

    .element {
        	@include backgroundGradient([settings]);
    }

## Backgroundsize

    body {
        @include background-image('pattern');
    }

## Set a rem font size with pixel fallback

    p {
        @include font-size(14px)
    }

## Breakpoints

    .sidebar {
        width: 60%;
        float: left;
        margin: 0 2% 0 0;

        @include bp-small {
            width: 100%;
            float: none;
            margin: 0;
        }
    }

## SVG background images with PNG and retina fallback

    body {
        @include background-image('pattern');
    }

## Animations and keyframes

    @include keyframes(slide-down) {
        0% { opacity: 1; }
        90% { opacity: 0; }
    }

    .element {
        width: 100px;
        height: 100px;
        background: black;
        @include animation('slide-down 5s 3');
    }

## Transitions

    a {
        color: gray;
        @include transition(color .3s ease);

        &:hover {
            color: black;
        }
    }

## Cross browser opacity

    .faded-text {
        @include opacity(0.8);
    }

## Clearfix

    .container-with-floated-children {
        @extend %clearfix;
    }

## Visually hide an element

    <button class="mobile-navigation-trigger">
        <b class="visually-hidden">Open the navigation</b>
        <img src="img/mobile-navigation-icon.svg">
    </button>

    .visually-hidden {
        @extend %visuallyhidden;
    }
