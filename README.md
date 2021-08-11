# Debugging DaNIS3H Modules
A simple way to inspect and debug DaNIS3H Modules at the bottom of an Ashiva Scaffold.

DaNIS3H Modules may be straightforwardly inspected which makes debugging them much easier:

```
echo '<pre style="text-align: left;">';

// PAGE MODULES
print_r($Page_Modules); // <= See the entire $Page_Modules output

// PAGE MODULES REGISTER
print_r($Page_Modules['Register']); // <= See the $Page_Modules Register
print_r(array_keys($Page_Modules['Register'])); // <= See which Modules are Registered
print_r($Page_Modules['Register']['SB_Colour_Charts']); // <= See the SB_Colour_Charts Module entry of the $Page_Modules Register

// MISCELLANEOUS
print_r(getPageModuleList($Page_Modules['Register'])); // <= No idea what this is...

// INDIVIDUAL DaNIS3H MODULES
print_r(${'<[SB_Body_Data]>'});
print_r(${'<[SB_nextPage]>'});
print_r(${'<[Ash_Site_Search]>'});

// INDIVIDUAL DaNIS3H Modules (WITH STRONG MODIFIERS)
print_r(${'<[SB_Notice::Brexit]>'});
print_r(${'<[SB_Notice::Covid_19]>'});

// SPECIFIC COMPONENTS FROM INDIVIDUAL DaNIS3H MODULES
print_r(${'<Markup[@]SB_Body_Data>'});
print_r(${'<Markup[@]SB_nextPage>'});
print_r(${'<Markup[@]Ash_Site_Search>'});

// SPECIFIC COMPONENTS FROM INDIVIDUAL DaNIS3H MODULES (WITH STRONG MODIFIERS)
print_r(${'<Markup[@]SB_Notice::Brexit>'});
print_r(${'<Markup[@]SB_Notice::Covid_19>'});

// PRIMECOMPONENTS FROM INDIVIDUAL DaNIS3H MODULES
print_r(${'<SB_Body_Data>'});
print_r(${'<SB_nextPage>'});
print_r(${'<Ash_Site_Search>'});

// PRIMECOMPONENTS FROM INDIVIDUAL DaNIS3H MODULES (WITH STRONG MODIFIERS)
print_r(${'<SB_Notice::Brexit>'});
print_r(${'<SB_Notice::Covid_19>'});


// print_r($Page_Modules['Register']['SB_Body_Data']['Attributes']);
// print_r(array_keys($Page_Modules['Styles']));
// print_r(array_keys(${'<[SB_Translations]>'}['Components']));
// print_r(array_keys($Page_Modules['Data']));
// print_r($Page_Modules['Scripts']);

echo '</pre>';

```


