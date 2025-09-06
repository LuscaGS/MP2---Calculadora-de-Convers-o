import React, { useState } from "react";
import { Text, TextInput, View, TouchableOpacity, StyleSheet, ScrollView } from "react-native";

export default function App() {
  const [celsius, setCelsius] = useState("");
  const [fahrenheit, setFahrenheit] = useState(null);

  const [kmh, setKmh] = useState("");
  const [mph, setMph] = useState(null);

  const convertTemperature = () => {
    const c = parseFloat(celsius);
    if (!isNaN(c)) {
      setFahrenheit(((c * 9) / 5 + 32).toFixed(2));
    } else {
      setFahrenheit(null);
    }
  };

  const convertSpeed = () => {
    const k = parseFloat(kmh);
    if (!isNaN(k)) {
      setMph((k * 0.621371).toFixed(2));
    } else {
      setMph(null);
    }
  };

  return (
    <ScrollView contentContainerStyle={styles.container}>
      <Text style={styles.title}>Calculadora de Conversão</Text>

      <View style={styles.card}>
        <Text style={styles.cardTitle}>Temperatura (°C → °F)</Text>
        <TextInput
          style={styles.input}
          placeholder="Digite em °C"
          placeholderTextColor="#aaa"
          keyboardType="numeric"
          value={celsius}
          onChangeText={setCelsius}
        />
        <TouchableOpacity style={styles.button} onPress={convertTemperature}>
          <Text style={styles.buttonText}>Converter</Text>
        </TouchableOpacity>
        {fahrenheit !== null && (
          <Text style={styles.result}>{celsius} °C = {fahrenheit} °F</Text>
        )}
      </View>

      <View style={styles.card}>
        <Text style={styles.cardTitle}>Velocidade (km/h → mph)</Text>
        <TextInput
          style={styles.input}
          placeholder="Digite em km/h"
          placeholderTextColor="#aaa"
          keyboardType="numeric"
          value={kmh}
          onChangeText={setKmh}
        />
        <TouchableOpacity style={styles.button} onPress={convertSpeed}>
          <Text style={styles.buttonText}>Converter</Text>
        </TouchableOpacity>
        {mph !== null && (
          <Text style={styles.result}>{kmh} km/h = {mph} mph</Text>
        )}
      </View>
    </ScrollView>
  );
}

const styles = StyleSheet.create({
  container: {
    flexGrow: 1,
    justifyContent: "center",
    alignItems: "center",
    backgroundColor: "#121212",
    padding: 20,
  },
  title: {
    fontSize: 26,
    fontWeight: "bold",
    marginBottom: 20,
    color: "#ffffff",
  },
  card: {
    width: "100%",
    backgroundColor: "#1e1e1e",
    borderRadius: 15,
    padding: 20,
    marginBottom: 20,
    shadowColor: "#000",
    shadowOpacity: 0.4,
    shadowOffset: { width: 0, height: 2 },
    shadowRadius: 6,
    elevation: 3,
  },
  cardTitle: {
    fontSize: 20,
    fontWeight: "600",
    marginBottom: 10,
    color: "#90caf9",
  },
  input: {
    borderWidth: 1,
    borderColor: "#333",
    borderRadius: 10,
    padding: 10,
    marginBottom: 10,
    fontSize: 16,
    backgroundColor: "#2c2c2c",
    color: "#fff",
  },
  button: {
    backgroundColor: "#1e88e5",
    padding: 12,
    borderRadius: 10,
    alignItems: "center",
    marginBottom: 10,
  },
  buttonText: {
    color: "#fff",
    fontSize: 16,
    fontWeight: "bold",
  },
  result: {
    fontSize: 18,
    fontWeight: "bold",
    color: "#4caf50",
    marginTop: 5,
  },
});
