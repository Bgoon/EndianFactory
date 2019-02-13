# EndianFactory

기본 자료형의 **빅-엔디안**과 **리틀-엔디안**끼리 변환하는 함수를 제공하는 라이브러리입니다.

제공하는 함수의 예시는 다음과 같습니다.

```{.cs}
    public static byte[] ToNetBytes(this bool value);
    public static byte[] ToNetBytes(this short value);
    public static byte[] ToNetBytes(this int value);
    public static byte[] ToNetBytesWithSize(this string value, Encoding encoding);
    
    public static bool ToLocalBoolean(this byte[] data, int startIndex = 0);
    public static short ToLocalInt16(this byte[] data, int startIndex  =  0);
    public static int ToLocalInt32(this byte[] data, int startIndex  =  0);
    public static string ToLocalStringWithSize(this byte[] data, Encoding encoding);
   
    public  static  byte[] Reverse(this  byte[] data, int  startIndex, int  size); 
```
<br>
함수명 명명 규칙은 다음과 같습니다.

 - Local Variable은 리틀-엔디안을 사용한다고 가정합니다. 
 - Net Variable은 빅-엔디안을 사용한다고 가정합니다.
