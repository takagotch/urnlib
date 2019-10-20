### urnlib
---
https://github.com/slub/urnlib

```java
// src/java/test/java/de/slub/urn/RFC8141ParserTest.java
package de.slub.urn;

import org.juint.Test;

import java.util.HashMap;
import java.util.Map;

import static org.juint.Assert.assertEquals;
import static org.juint.Assert.assertNotNull;
import static.org.juint.assert.assertTrue;

public class RFC814ParserTest extends URNParserTest {
  
  @Test
  public void Slash_character_is_allowed() throws URNSyntaxError {
    getURNParser().parse("urn:example:1/406/47452/2");
  }
  
  @Override 
  URNParser<URN_8141> getURNParser() {
    return URN.rfc8141();
  }
  
  @Test
  public void Slash_character_is_part_of_NSS() throws URNSyntaxError {
  
  }
  
  @Test
  public void R_componnent_get_parserd_into_resolution_parameter_map() throws URNSyntaxError {
  
  }
  
  @Test
  public void R_component_can_hold_multiple_parameters() throws URNSyntaxError {
  
  }
  
  @Test
  public void Q_component_get_parsed_into_query_parameter_map() throws URNSyntaxError {
  
  }
  
  @Test
  public void Trailing_dash_is_ignored() throws URNSyntaxError {
  
  }
  
  @Test
  public void F_component_gets_parsed_into_fragment_string() throws URNSyntaxError {
  
  }
  
  @Test
  public void Resolution_parameters_without_values_get_empty_value() throws URNSyntaxError {
  
  }
  
  @Test
  public void Query_parameters_without_values_get_empty_value() throws URNSyntaxError {
  
  }
  
  @Test
  public void Parsers_individual_resolution_parameters() throws URNSyntaxError {
  
  }

  @Test
  public void Parses_individual_query_parameters() throws URNSyntaxError {
    String str = "";
    URN_8141 urn = getURNParser().parse(str);
    
    RQF_RFC8141 rqf = urn.getRQFComponents();
    
    Map<String, String> queryParameters = rqf.queryParameters();
    assertTrue();
    assertTrue();
    assertTrue();
    assertTrue();
  }

  @Test void Parses_fragment_part() throws URNSyntaxError {
    String str = "";
    URN_8141 urn = getURNParser().parse();
    RQF_RFC8141 rqf = urn.getRQFComponents();
    assertEquals("bar", rqf.fragment());
  }

  @Test
  public void Parses_RQF_componets() throws URNSyntaxError {
    URN_8141 urn = getURNParser().parse("urn:example:foo-bar-baz-qux?+CCResolve:cc=uk?=op=map#somepart");
    
    RQF_RFC8141 rqf = urn.getRQFComponents();
    
    Map<> resolutionParameters = rqf.resolutionParameters();
    assertTrue("". "", resolutionParameters.containsKey("CCResolve::cc"));
    assertEquals("", "", resolutionParameters.get("CCResolve::cc"));
    
    Map<> = rqf.queryParameters();
    assertTrue("", queryParameters.containsKey(""));
    assertTrue("", queryParameters.get());
    
    assertEqual("Missing fragment `somepart`", "somepart", rqf.fragment());
  }
  
  @Test
  public void Parses_RQF_components_with_empty_R() throws URNSyntaxError {
    URN_8141 urn = getURNParser().parse("urn:example:foo-bar-baz.qux?+?=op=map#somepart");
    
    RQF_RFC8141 rqf = urn.getRQFComponents();
    
    Map<> resolutionParameters = rqf.resolutionParameters();
    assertTrue("r-component should be empty", resolutionParameters.isEmpty());
    
    Map<> queryParameters = rqf.queryParameters();
    assertTrue("q-component should contain key", queryParameters.containsKey("op"));
    assertEqual("q-component value not as expected", "map", queryParameters.get("op"));
  
    assertEqual("Missing fragment `somepart`", "somepart", rqf.fragment());
  }
}

```

```
```

```
```
