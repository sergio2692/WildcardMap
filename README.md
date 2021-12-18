# WildcardMap
Documentation WildcardMap Ue4 plugin
WildcardMap is a simple but powerful tool for UE4, it is giving the possibility to have a generic TMap that accept every type of data in blueprint.
# How to use
Activate the plugin, and then will be enabled a new type of property "WildcardMap", use it as property of any class in blueprint, and then it will give two functions "Get" and "Add"
![image](https://user-images.githubusercontent.com/13841147/146653606-30a0cb8f-2e3c-4ddc-bba1-e6c194c2e261.png)
# Add
The function Add accept two parameters and is used for adding an element to the Map, the key is a gameplaytag and the value is a wildcard that can accept every type of value.
# Get
The function Get retrieve the element associated with the gameplaytag if it is stored inside the map, there is a bool to check if it was found, it's important to use a branch because when we use the element we must be sure that the key looked for contains an element of the same type and wich it is really stored inside the map.

# Conclusion
The functionality is pretty the same as a standard TMap so it's pretty easy to understand how to use it, but please note that a Map of this type doesn't store the element and it contains void pointers not recognized from the garbage collector, so if the last reference of the uproperty is inside this map then will be garbage collected.
Use it to get references through blueprint without casting and to make easy passing generic data through objects.
