# callbydailerpaid

import 'package:flutter/material.dart';
import 'package:url_launcher/url_launcher.dart';

class CallScreen extends StatefulWidget {
  final String number;
  const CallScreen({super.key, this.number = ''});

  @override
  State<CallScreen> createState() => CallScreenState();
}

class CallScreenState extends State<CallScreen> {

// method 1
  // var number = 8840591006;

  // callnumber(String number) async {
  //   Uri dialNumber = Uri(scheme: 'tel', path: number);
  //   await launchUrl(dialNumber);
  // }


  //method 2

  Uri dualnumber = Uri(scheme: 'tel', path: '7525827482');

  callnumbere() {
    launchUrl(dualnumber);
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Call Example'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            ElevatedButton(
              onPressed: () {
                // callnumber(number.toString());
                callnumbere();
              },
              child: const Text('Call using Dialer'),
            ),
          ],
        ),
      ),
    );
  }
}
