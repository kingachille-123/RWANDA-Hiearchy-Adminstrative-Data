# RWANDA-Hiearchy-Adminstrative-Data
This contains a .json file for the RWANDA hiearchy adminstrative data from the district to village this can help developers who want to use the cascading dropdowns select for the adminstrative data of RWANDA in their project mainly those who use c# to get easy access and easy implmentation

## How to use
1. Download the .json file from the repository.
2. In your C# project, add the .json file to your project directory.
3. Use a JSON parsing library (like Newtonsoft.Json) to read and parse the .json file into your desired data structure (e.g., classes or dictionaries).
4. Implement the cascading dropdowns in your application using the parsed data to populate the dropdown options based on the selected values.
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Newtonsoft.Json;
public class AdministrativeData
{
    public string District { get; set; }
    public List<string> Sectors { get; set; }
    public List<string> Cells { get; set; }
    public List<string> Villages { get; set; }
}
public class Program
{
    public static void Main()
    {
        string jsonFilePath = "path_to_your_json_file.json";
        string jsonData = File.ReadAllText(jsonFilePath);
        List<AdministrativeData> adminData = JsonConvert.DeserializeObject<List<AdministrativeData>>(jsonData);
        
        // Now you can use adminData to populate your cascading dropdowns
    }
}
```Make sure to replace `"path_to_your_json_file.json"` with the actual path to your .json file in your project. This code snippet demonstrates how to read and parse the .json file into a list of `AdministrativeData` objects, which you can then use to populate your cascading dropdowns in your application.
## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
## Contributing
Contributions are welcome! If you have any improvements or additions to the data, please feel free to submit a pull request or open an issue for discussion.
## Contact
If you have any questions or need further assistance, please feel free to contact the repository owner or open an issue in the repository.
## Acknowledgments
- Special thanks to the developers who have used this data in their projects and provided feedback for improvements
- Thanks to the open-source community for providing tools and libraries that make working with JSON data easier in C#.
## Disclaimer
This data is provided "as is" without any warranties or guarantees. The accuracy and completeness of the data cannot be guaranteed, and the repository owner is not responsible for any issues that may arise from using this data in your projects. Always verify the data and use it at your own risk.


Developed by AKUZWE Aine Achille - [GitHub](kingachille-123) - [LinkedIn](https://www.linkedin.com/in/akuzwe-aine-achille-9a1b4b1b2/)


developed with ❤️ in Rwanda