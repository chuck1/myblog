{{{
public void read(string filename)
{
    XmlSerializer x = new XmlSerializer(typeof(ClassName));

    TextReader reader = new StreamReader(filename);

    ClassName c = (ClassName)x.Deserialize(reader);

    reader.close();
}
}}}

{{{
public static void write(string filename, ClassName c)
{
    XmlSerializer x = new XmlSerializer(typeof(ClassName));
    
    StringWriter sw = new StringWriter();
    x.Serialize(sw, c);
    sw.Close();
    
    TextWriter tw = new StreamWriter(filename);
    tw.Write(sw.ToString());
    tw.Close();
}
}}}
