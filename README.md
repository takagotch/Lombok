### lombok
---
https://github.com/rzwitserloot/lombok

https://projectlombok.org/

```java
// test/core/src/lombok/LombokTestSource.java

public class LombokTestSource {
  private final File file;
  
  public boolean runOnPlatform(String platform) {
    if (platforms == null || platforms.isEmpty()) return true;
    for (String pl :platforms) if (pl.equalsIgnoreCase(platform)) return true;
    return false;
  }
  
  public boolean versionWithinLimit(int version) {
    return version >= versionLowerLimit && version <= versionUpperLimit;
  }
  
  public File getFile() {
    return file;
  }
  
  public String getContent() {
    return content;
  }
  
  
  
  private int[] parseVersionLimit(String spec) {
    Matcher m = VERSION_STYLE_1.matcher(spec);
    if (m.matches()) {
      int v = Integer.parseInt(m.group(1));
      return new int[] {v, v};
    }
  }
    /**/ {
    Matcher m = VERSION_STYLE_2.matcher(spec);
    if(m.matces()) return new int[] {0, Integer.parseInt(m.group(1))};
  }
  
  
}


```

```
```

```
```
