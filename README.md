System.Text.GB2312Encoding implementation target on .NET Standard 2.0.

We can use it on Xamarin projects.

This project is compiled with VS2017

Usage like following:

string StreamToString(Stream ss)
{
    var ret = "";
    var encoding = GB2312Encoding.Instance;
    using (var reader = new StreamReader(ss, encoding))
    {
        ret = reader.ReadToEnd();
    }
    return ret;
}
