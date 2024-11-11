# mast-poe
FINAL-POE--RESTURANT
IN THIS FINAL PART OF THE POE CRUCIAL CHANGES WERE MADE AFTER GETTING FEEDBACK FROM ASSIGNMEENT PART 2. IN THS FINAL POE
WE USED VISUAL STUDIO CODE AND WE USED TYPESCRIPT AND ANDROID STUDIO TO USE OUR EXPO GO PLATFORM. IN THE CODES WE HAD 1 ERORR MAINLY FOR
NAVIGATION WHICH DISRUPTS THE EMMULATOR. In these implemented changes they were changes in the files created
1) App.tsx
2) Homescreen.tsx
3) MenuScreen.tsx
4) DrinksScreen.tsx
5) StartersScreen.tsx
6) MainScreen.tsx
7) DessertSreen.tsx
8) PaymentScreen.tsx Such changes were made as this POE used React native and typescript installing our react-native/naviggation in the terminals.
Below is the code us for App.tsx
/ App.tsx
import React from 'react';
import { NavigationContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';
import HomeScreen from './HomeScreen';
import MenuScreen from './/MenuScreen';
import DrinkScreen from './DrinksScreen';
import StartersScreen from './StartersScreen';
import MainScreen from './MainScreen';
import DessertScreen from './DessertScreen';

const Stack = createStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator screenOptions={{ headerShown: false }}>
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Menu" component={MenuScreen} />
        <Stack.Screen name="Drinks" component={DrinkScreen} />
        <Stack.Screen name="Starters" component={StartersScreen} />
        <Stack.Screen name="Main" component={MainScreen} />
        <Stack.Screen name="Desset" component={DessertScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}``

export default App;
this is the example off the changes that were implemented
