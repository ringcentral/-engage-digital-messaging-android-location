Engage Digital Messaging Maps SDK Customization
===============================================

The Engage Digital Messaging Maps SDK is customizable either programmatically or using the Android resource folder (XML).

This file shows a list of attributes you can override in order to customize the threads list and the chat.

# Attributes < drawable />

### sendButtonIcon
A drawable for the send button displayed in the maps activity.

XML attribute name: `rc_maps_send_button`

Programmatically: use the `setSendButtonIcon(int sendButtonIcon)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/vTyh2Cpt/Capture-d-e-cran-2021-12-17-a-14-38-21.png"/>
</p>


# Attributes < color />

Colors must be in hex format, e.g. `007AFF` or `#007AFF`.

### navigationBarTitleColor
Text color for the navigation bar title displayed in the maps view.

XML attribute name: `rc_maps_navigation_bar_title_color`

Programmatically: use the `setNavigationBarTitleColor(int navigationBarTitleColor)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/9XBjp290/navigationbartitlecolor.png"/>
</p>

### navigationBarBackgroundColor
Color for the navigation bar displayed in the maps view.

XML attribute name: `rc_maps_navigation_bar_backgroung_color`

Programmatically: use the `setNavigationBarBackgroundColor(int navigationBarBackgroundColor)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/XJ3zGZQ8/Capture-d-e-cran-2021-12-17-a-13-15-37.png"/>
</p>


### navigationBarBackIconColor
Color for the navigation bar back icon displayed in the maps view.

XML attribute name: `rc_maps_navigation_bar_back_icon_color`

Programmatically: use the `setNavigationBarBackIconColor(int navigationBarBackIconColor)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/MTF1kNMQ/icon-color.png"/>
</p>

### navigationBarSearchIconColor
Color for the navigation bar search icon displayed in the maps view.

XML attribute name: `rc_maps_navigation_bar_search_icon_color`

Programmatically: None

Result:
<p align="center">
    <img src="https://i.postimg.cc/Fz0bjGzk/search-color.png"/>
</p>

### sendButtonIconColor
Color for the send button icon displayed in the maps view.

XML attribute name: `rc_maps_send_button_icon_color`

Programmatically: use the `setSendButtonIconColor(int sendButtonIconColor)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/QtTYyQVh/Capture-d-e-cran-2021-12-17-a-14-40-44.png"/>
</p>

### sendButtonBackgroundColor
Color used for the background of the send button that is displayed in the maps view.

XML attribute name: `rc_maps_send_button_background_color`

Programmatically: use the `setSendButtonBackgroundColor(int sendButtonBackgroundColor)` method

Result:
 <p align="center">
   <img src="https://i.postimg.cc/tRD4gW2B/Capture-d-e-cran-2021-12-17-a-14-25-03.png"/>
</p>


# Attributes < dimen />

### navigationBarTitleSize
Text size for the title of the navigation bar displayed in the maps view.

XML attribute name: `rc_maps_navigation_bar_title_text_size`

Programmatically: use the `setNavigationBarTitleSize(int navigationBarTitleSize)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/HWKs5d1M/title-size.png"/>
</p>

# Typeface

### navigationBarTitleFont
Font applied to the navigation bar title displayed in the maps view.

XML attribute name: None

Programmatically: use the `setNavigationBarTitleFont(Typeface navigationBarTitleFont)` method

Result:
<p align="center">
    <img src="https://i.postimg.cc/PrPTrcLq/font.png"/>
</p>
