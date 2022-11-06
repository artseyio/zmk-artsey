# shields

This directory contains the specific ZMK ARTSEY impementations for various keyboards. Please see the sub directories for specific implementation details.

If you are interested in using the custom layer for gaming. Below is a keymap by @granitrocky that works with Doom Eternal.
You can copy/paste this into your .keymap file BEFORE you include `artsey.dtsi`


```c
//Copied from the base file for reference only
#define LAYER_ID_GLOBAL -1
#define LAYER_ID_BASE 0
#define LAYER_ID_NUMBERS 1
#define LAYER_ID_SYMBOLS 2
#define LAYER_ID_PARENTHETICALS 3
#define LAYER_ID_NAVIGATION 4
#define LAYER_ID_BT_SEL 5
#define LAYER_ID_CUSTOM 6
#define LAYER_ID_BIG_SYM 7
#define LAYER_ID_BIG_FUNCTION 8

\\This variable sets the Global Combos like 'enter' and 'space' to only be active on the specific layers.
\\Note that layer 6, 'Custom', is missing. This means we can set a lower combo timeout for that layer.
#define GLOBAL_COMBO_LAYER_FILTER LAYER_ID_BASE LAYER_ID_NUMBERS LAYER_ID_SYMBOLS LAYER_ID_PARENTHETICALS LAYER_ID_NAVIGATION LAYER_ID_BT_SEL LAYER_ID_BIG_SYM LAYER_ID_BIG_FUNCTION

\\This sets the timeout to a lower amount to reduce input latency.
\\ Note that setting this higher will make multi key combos easier to press at the cost of increased latency
#define TIMEOUT_COMBO_CUSTOM_LAYER 50


#define ARTSEY_LAYER_CUSTOM                                             \
    custom {                                                            \
			label = "Custom";                                           \
			bindings = <                                                \
				&kp LSHIFT   &kp Q  &kp W   &kp E                       \
				&kp SPACE    &kp A  &kp S   &kp D                       \
                >;                                                      \
		};

#define CUSTOM_COMBOS \
    custom_combo_4_1    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_T KEY_S KEY_O>; bindings = <&kp SPACE>;  }; \
    custom_combo_4_2    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_E KEY_Y KEY_I KEY_O>; bindings = <&kp SPACE>;  }; \
    custom_combo_3_1    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_T KEY_S>;       bindings = <&kp TAB>;    }; \
    custom_combo_3_2    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_T KEY_O>;       bindings = <&kp LCTRL>;  }; \
    custom_combo_3_3    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_T KEY_S KEY_O>;       bindings = <&kp LALT>;   }; \
    custom_combo_2_1    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_T>;             bindings = <&kp R>;      }; \
    custom_combo_2_2    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_S>;             bindings = <&kp V>;      }; \
    custom_combo_2_3    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_A KEY_O>;             bindings = <&kp F>;      }; \
    custom_combo_2_4    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_T KEY_S>;             bindings = <&kp G>;      }; \
    custom_combo_2_5    { layers = <LAYER_ID_CUSTOM>; timeout-ms = <TIMEOUT_COMBO_CUSTOM_LAYER>; key-positions = <KEY_T KEY_O>;             bindings = <&kp C>;      };
```
