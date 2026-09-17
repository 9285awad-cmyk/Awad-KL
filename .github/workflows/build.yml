import 'package:flutter/material.dart';
import 'package:flutter_localizations/flutter_localizations.dart';
import 'package:http/http.dart' as http;
import 'dart:convert' as json;

// لتفعيل شاشة الصيانة: للتحكم في وضع الصيانة
const bool isUnderMaintenance = false;

void main() {
  runApp(const FootballApp());
}

class FootballApp extends StatelessWidget {
  const FootballApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Awad KL',
      debugShowCheckedModeBanner: false,
      locale: const Locale('ar', 'SA'),
      supportedLocales: const [Locale('ar', 'SA')],
      localizationsDelegates: const [
        GlobalMaterialLocalizations.delegate,
        GlobalWidgetsLocalizations.delegate,
        GlobalCupertinoLocalizations.delegate,
      ],
      theme: ThemeData(
        primarySwatch: Colors.green,
        scaffoldBackgroundColor: const Color(0xFF121212),
      ),
      home: isUnderMaintenance ? const MaintenanceScreen() : const HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  const HomeScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Awad KL - الدوري'),
        backgroundColor: Colors.green[800],
      ),
      body: const Center(
        child: Text(
          'أهلاً بك يا عوض في تطبيقك الرياضي',
          style: TextStyle(color: Colors.white, fontSize: 18),
        ),
      ),
    );
  }
}

class MaintenanceScreen extends StatelessWidget {
  const MaintenanceScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Padding(
          padding: const EdgeInsets.all(20.0),
          child: Text(
            'التطبيق تحت الصيانة حالياً، عودوا قريباً.',
            style: TextStyle(color: Colors.yellow[700], fontSize: 20),
            textAlign: TextAlign.center,
          ),
        ),
      ),
    );
  }
}
