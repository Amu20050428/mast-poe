# mast-poe
FINAL-POE--RESTURANT
below is the youtube video explaing my code and emulator/design
https://youtu.be/APE8qdMRpTo 
https://youtu.be/APE8qdMRpTo
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
followed by the home screen
import React from 'react';
import { View, Text, TouchableOpacity, ImageBackground, StyleSheet, Button } from 'react-native';
import Navigation from './navigation';

const HomeScreen = ({ navigation }) =>{
  return (
    <ImageBackground source={require('../assets/home_background.jpg')} style={styles.background}>
      <View style={styles.overlay}>
        {/* Welcome and subtitle */}
        <Text style={styles.welcomeText}>Welcome to Christopher's Restaurant</Text>
        <Text style={styles.subText}>YOUR TASTE YOUR WORLD</Text>

        {/* Buttons to explore and exit */}
        <TouchableOpacity style={styles.button} onPress={() => navigation.navigate('Menu')}>
          <Text style={styles.buttonText}>EXPLORE RESTAURANT</Text>
        </TouchableOpacity>

        <TouchableOpacity style={styles.button} onPress={() => console.log('Exit App')}>
          <Text style={styles.buttonText}>EXIT APP</Text>
        </TouchableOpacity>

        {/* Navigation buttons to each course */}
        <View style={styles.navButtons}>
          <Button
            title="Go to Drinks"
            onPress={() => navigation.navigate('Drinks')}
            color="#333"
          />
          <Button
            title="Go to Starters"
            onPress={() => navigation.navigate('Starters')}
            color="#333"
          />
          <Button
            title="Go to Main"
            onPress={() => navigation.navigate('Main')}
            color="#333"
          />
          <Button
            title="Go to Desserts"
            onPress={() => navigation.navigate('Desserts')}
            color="#333"
          />
        </View>
      </View>
    </ImageBackground>
  );
};

const styles = StyleSheet.create({
  background: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
  },
  overlay: {
    alignItems: 'center',
    backgroundColor: 'rgba(0, 0, 0, 0.5)',
    padding: 20,
    borderRadius: 10,
    width: '90%',
  },
  welcomeText: {
    color: '#fff',
    fontSize: 24,
    fontWeight: 'bold',
    textAlign: 'center',
    marginBottom: 10,
  },
  subText: {
    color: '#fff',
    fontSize: 16,
    marginBottom: 20,
    textAlign: 'center',
  },
  button: {
    backgroundColor: '#333',
    paddingVertical: 10,
    paddingHorizontal: 40,
    borderRadius: 5,
    marginTop: 10,
  },
  buttonText: {
    color: '#fff',
    fontSize: 18,
    textAlign: 'center',
  },
  navButtons: {
    marginTop: 20,
    width: '100%',
    justifyContent: 'space-around',
    alignItems: 'center',
  },
});

export default HomeScreen;

