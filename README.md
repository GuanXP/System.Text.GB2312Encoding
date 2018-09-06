# Welcome to System.Text.GB2312Encoding

System.Text.GB2312Encoding is an implementation of System.Text.Encoding for charset GB2312 target on .NET Standard 2.0.

This project is compiled with VS2017.

# Usage


    static string StreamToString(Stream ss)
    {
    	var ret = "";
    	var encoding = GB2312Encoding.Instance;
    	using (var reader = new StreamReader(ss, encoding))
    	{
    		ret = reader.ReadToEnd();
    	}
    	return ret;
    }
