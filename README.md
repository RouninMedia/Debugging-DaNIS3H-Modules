# Inspecting and Debugging DaNIS3H Modules
A simple way to inspect and debug DaNIS3H Modules at the bottom of an Ashiva Scaffold.

DaNIS3H Modules may be straightforwardly inspected which makes debugging them much easier:

```
echo '<pre style="text-align: left;">';

// FULL PAGE MODULES
print_r($Page_Modules); // <= See the entire $Page_Modules output

// FULL ASSETS (STYLES, SCRIPTS, DATA ETC.)
print_r($Page_Modules['Scripts']);
print_r($Page_Modules['Vectors']);

// SHOW MODULES WHICH INCLUDE SPECIFIC ASSETS
print_r(array_keys($Page_Modules['Styles']));
print_r(array_keys($Page_Modules['Data']));

// PAGE MODULES REGISTER
print_r($Page_Modules['Register']); // <= See the $Page_Modules Register
print_r(array_keys($Page_Modules['Register'])); // <= See which Modules are Registered
print_r($Page_Modules['Register']['SB_Colour_Charts']); // <= See the SB_Colour_Charts Module entry of the $Page_Modules Register
print_r($Page_Modules['Register']['SB_Body_Data']['Attributes']); // See just the Attributes of the SB_Body_Data Module entry of the $Page_Modules Register

// MISCELLANEOUS
print_r(getPageModuleList($Page_Modules['Register'])); // <= No idea what this is...

// INDIVIDUAL DaNIS3H MODULES
print_r(${'<[SB_Body_Data]>'});
print_r(${'<[SB_nextPage]>'});
print_r(${'<[Ash_Site_Search]>'});

// INDIVIDUAL DaNIS3H Modules (WITH STRONG MODIFIERS)
print_r(${'<[SB_Notice::Brexit]>'});
print_r(${'<[SB_Notice::Covid_19]>'});

// SHOW PRIMECOMPONENTS FROM INDIVIDUAL DaNIS3H MODULES
print_r(${'<SB_Body_Data>'});
print_r(${'<SB_nextPage>'});
print_r(${'<Ash_Site_Search>'});

// SHOW PRIMECOMPONENTS FROM INDIVIDUAL DaNIS3H MODULES (WITH STRONG MODIFIERS)
print_r(${'<SB_Notice::Brexit>'});
print_r(${'<SB_Notice::Covid_19>'});

// SHOW WHICH COMPONENTS AN INDIVIDUAL DaNIS3H MODULE HAS
print_r(array_keys(${'<[SB_Translations]>'}['Components']));

// SHOW SPECIFIC COMPONENT FROM INDIVIDUAL DaNIS3H MODULE
print_r(${'<Markup[@]SB_Body_Data>'});
print_r(${'<Markup[@]SB_nextPage>'});
print_r(${'<Markup[@]Ash_Site_Search>'});

// SHOW SPECIFIC COMPONENT FROM INDIVIDUAL DaNIS3H MODULE (WITH STRONG MODIFIERS)
print_r(${'<Markup[@]SB_Notice::Brexit>'});
print_r(${'<Markup[@]SB_Notice::Covid_19>'});

// SHOW SPECIFIC CUSTOM COMPONENT FROM INDIVIDUAL DaNIS3H MODULE
print_r(${'<Open_Control_Pad_Button[@]Ashiva_Control_Pad>'});

echo '</pre>';

```


