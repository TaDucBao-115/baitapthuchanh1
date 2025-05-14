# baitapthuchanh1
import 'package:flutter/material.dart';

void main() {
  runApp(MyGitHubApp());
}

class MyGitHubApp extends StatelessWidget {
  const MyGitHubApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'GitHub App',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: GitHubHomePage(),
    );
  }
}

class GitHubHomePage extends StatefulWidget {
  const GitHubHomePage({Key? key}) : super(key: key);

  @override
  GitHubHomePageState createState() => GitHubHomePageState();
}

class GitHubHomePageState extends State<GitHubHomePage> {
  String username = "Tạ Đức Bảo - CN2303A"; // Tên người dùng
  String location = "Mong muốn và định hướng của Bạn là gì sau khi học xong môn học là gì"; // Vị trí

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('GitHub Profile'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const CircleAvatar(
              radius: 50,
              backgroundImage: NetworkImage(
                  'https://via.placeholder.com/150'), // Placeholder ảnh
            ),
            const SizedBox(height: 20),
            Text(
              username,
              style: const TextStyle(fontSize: 24, fontWeight: FontWeight.bold),
            ),
            const SizedBox(height: 10),
            Text(
              location,
              style: const TextStyle(fontSize: 18, color: Colors.grey),
            ),
            const SizedBox(height: 20),
          ],
        ),
      ),
    );
  }
}
