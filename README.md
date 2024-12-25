# Unhandled JSON Decoding Exception in Dart Asynchronous Operation

This repository demonstrates a common error in asynchronous Dart applications and presents its solution. The error involves failing to handle potential exceptions during JSON decoding within an asynchronous function, leading to unexpected app behavior or crashes.

## The Problem

The provided `bug.dart` file shows the incorrect approach: a simple `try-catch` block around the `http.get` request handles network errors but ignores potential `jsonDecode` exceptions. If the server returns malformed JSON, the application will crash or behave unexpectedly.

## The Solution

The `bugSolution.dart` file offers a more robust approach. It handles the `FormatException` thrown by `jsonDecode` if the response isn't valid JSON, providing a more graceful error handling mechanism.