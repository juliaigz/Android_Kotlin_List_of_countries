# Android_Kotlin_List_of_countries
### This is a project made in kotlin using ListView in Android Studio 

Step 1: 

Add view Binding in Build Gradle  

![image](https://github.com/juliaigz/Android_Kotlin_List_of_countries/assets/40221707/e94fdabb-c950-4115-a522-8bf45ee8201f)



Activity_main

![image](https://github.com/juliaigz/Android_Kotlin_List_of_countries/assets/40221707/13f2e93c-51f2-46bc-9fb9-74f345cadc1e)



MainActivity java 

![image](https://github.com/juliaigz/Android_Kotlin_List_of_countries/assets/40221707/05aaec71-4419-4bf9-91b5-92165854c106)



´´´Bash

class MainActivity : AppCompatActivity() {

    lateinit var  binding:ActivityMainBinding
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding = ActivityMainBinding.inflate(getLayoutInflater());
        setContentView(binding.getRoot());

        var arrayAdapter: ArrayAdapter<*>
        val paises = mutableListOf("Argentina", "Paraguay",
            "Bolivia","Peru","Ecuador","Brasil","Colombia","Venezuela","Uruguay")

        //val list1 = findViewById<ListView>(R.id.list1)
        val list1 = binding.list1

        arrayAdapter = ArrayAdapter(this,android.R.layout.simple_list_item_1,paises)
        list1.adapter = arrayAdapter
        //val text1 = findViewById<TextView>(R.id.text1)
        val text1 = binding.text1
        
        list1.setOnItemClickListener { parent, view, position, id ->
            val selectedItem = paises[position]
            if (selectedItem == "Argentina")  text1.text = "En Argentina hay 30.000.000 de habitantes"
            if (selectedItem == "Paraguay")  text1.text = "En Paraguay hay 7.000.000 de habitantes"
            if (selectedItem == "Bolivia")  text1.text = "En Bolivia hay hay 15.000.000 de habitantes"
            if (selectedItem == "Peru")  text1.text = "En Peru hay 33.000.000 de habitantes"
            if (selectedItem == "Ecuador")  text1.text = "En Ecuador hay 6.000.000 de habitantes"
            if (selectedItem == "Brasil")  text1.text = "En Brasil hay 80.000.000 de habitantes"
            if (selectedItem == "Colombia")  text1.text = "En Colombia hay 26.000.000 de habitantes"
            if (selectedItem == "Venezuela")  text1.text = "En Venezuela hay 32.000.000 de habitantes"
            if (selectedItem == "Uruguay")  text1.text = "En Uruguay hay 8.000.000 de habitantes"
        }
    }
}

´´´
