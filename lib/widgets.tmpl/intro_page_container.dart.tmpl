import 'package:flutter/material.dart';

enum IndicatorAlign {
  top,
  center,
  bottom,
  bottomLeft,
}

class PageIndicatorContainer extends StatefulWidget {
  final PageView pageView;

  final int length;

  final EdgeInsets padding;

  final IndicatorAlign align;

  final IndicatorShape shape;

  final Color indicatorColor;

  final Color indicatorSelectorColor;

  final double indicatorSpace;

  const PageIndicatorContainer({
    Key key,
    @required this.pageView,
    @required this.length,
    this.padding = const EdgeInsets.only(bottom: 10.0, top: 10.0),
    this.align = IndicatorAlign.bottom,
    this.indicatorColor = const Color(0xFFFFFFFF),
    this.indicatorSelectorColor = Colors.grey,
    this.indicatorSpace = 8.0,
    this.shape = IndicatorShape.defaultCircle,
  }) : super(key: key);

  @override
  PageContainerState createState() => PageContainerState();
}

class PageContainerState extends State<PageIndicatorContainer> {
  @override
  Widget build(BuildContext context) {
    var controller = pageView.controller;
    double height = widget.shape.height;
    Widget indicator = PageIndicator(
      controller: controller,
      length: widget.length,
      color: widget.indicatorColor,
      selectedColor: widget.indicatorSelectorColor,
      indicatorSpace: widget.indicatorSpace,
      indicatorShape: widget.shape,
      align: widget.align,
      reverse: pageView.reverse,
    );

    var align = widget.align;

    if (align == IndicatorAlign.bottom) {
      indicator = Positioned(
        left: 0.0,
        right: 0.0,
        bottom: widget.padding.bottom,
        height: height,
        child: indicator,
      );
    } else if (align == IndicatorAlign.bottomLeft) {
      indicator = Positioned(
        left: 72,
        bottom: widget.padding.bottom,
        height: height,
        child: indicator,
      );
    } else if (align == IndicatorAlign.top) {
      indicator = Positioned(
        left: 0.0,
        right: 0.0,
        top: widget.padding.top,
        height: height,
        child: indicator,
      );
    } else if (align == IndicatorAlign.center) {
      indicator = Center(
        child: Container(
          child: indicator,
          height: height,
        ),
      );
    }

    return Column(
      children: <Widget>[
        Flexible(
          child: Container(
            child: NotificationListener<ScrollNotification>(
              child: pageView,
              onNotification: _onScroll,
            ),
          ),
        ),

        Container(
          height: 40,
          width: double.infinity,
          child: Stack(
              children: <Widget>[
                indicator
              ],
          ),
        )
      ],
    );
  }

  PageView get pageView => widget.pageView;

  bool _onScroll(ScrollNotification notification) {
    setState(() {});
    return false;
  }

  void forceRefreshState() {
    this.setState(() {});
  }
}

abstract class IndicatorShape {
  const IndicatorShape._();

  static const defaultCircle = const CircleShape(12.0);

  static const defaultRoundRectangle = const RoundRectangleShape();

  static const defaultOval = const OvalShape();

  factory IndicatorShape.circle({double size = 12.0}) {
    return CircleShape(size);
  }

  factory IndicatorShape.roundRectangleShape({
    Size size = const Size(12.0, 12.0),
    Size cornerSize = const Size.square(3),
  }) {
    return RoundRectangleShape(
      cornerSize: cornerSize,
      size: size,
    );
  }

  factory IndicatorShape.oval({Size size = const Size(12, 8)}) {
    return OvalShape(size: size);
  }

  double get height;

  double get width;
}

class CircleShape extends IndicatorShape {
  final double size;
  const CircleShape(this.size) : super._();

  @override
  double get height => this.size;

  @override
  double get width => this.size;
}

class RoundRectangleShape extends IndicatorShape {
  final Size size;
  final Size cornerSize;

  const RoundRectangleShape({
    this.size = const Size(12, 12),
    this.cornerSize = const Size.square(3),
  }) : super._();

  @override
  double get height => this.size.height;

  @override
  double get width => this.size.width;
}

class OvalShape extends IndicatorShape {
  final Size size;
  const OvalShape({
    this.size = const Size(12, 4),
  }) : super._();

  @override
  double get height => this.size.height;

  @override
  double get width => this.size.width;
}

class PageIndicator extends StatefulWidget {
  final Color color;

  final Color selectedColor;

  final int length;

  final PageController controller;

  final double indicatorSpace;

  final IndicatorShape indicatorShape;

  final IndicatorAlign align;

  final bool reverse;

  const PageIndicator({
    Key key,
    this.color = const Color(0xFFFFFFFF),
    this.selectedColor = Colors.grey,
    @required this.controller,
    @required this.length,
    this.indicatorSpace = 5.0,
    this.indicatorShape = IndicatorShape.defaultCircle,
    this.align = IndicatorAlign.bottom,
    this.reverse = false,
  }) : super(key: key);

  @override
  _PageIndicatorState createState() => _PageIndicatorState();
}

class _PageIndicatorState extends State<PageIndicator> {
  PageController get controller => widget.controller;

  @override
  void initState() {
    super.initState();
  }

  @override
  void dispose() {
    super.dispose();
  }

  @override
  Widget build(BuildContext context) {
    CustomPainter indicatorPainter;

    IndicatorShape shape = widget.indicatorShape;

    bool reverse = widget.reverse;

    if (shape is OvalShape) {
      indicatorPainter = OvalPainter(
        color: widget.color,
        selectedColor: widget.selectedColor,
        count: widget.length,
        page: widget.controller.page ?? controller.initialPage.toDouble(),
        padding: widget.indicatorSpace,
        size: shape.size,
      );
    } else if (shape is RoundRectangleShape) {
      indicatorPainter = RRectPainter(
        color: widget.color,
        selectedColor: widget.selectedColor,
        count: widget.length,
        page: widget.controller.page ?? controller.initialPage.toDouble(),
        padding: widget.indicatorSpace,
        size: shape.size,
        cornerSize: shape.cornerSize,
      );
    } else if (shape is CircleShape) {
      indicatorPainter = CirclePainter(
        color: widget.color,
        selectedColor: widget.selectedColor,
        count: widget.length,
        page: widget.controller.page ?? controller.initialPage.toDouble(),
        padding: widget.indicatorSpace,
        radius: shape.size / 2,
      );
    }

    return IgnorePointer(
      child: RotatedBox(
        quarterTurns: reverse ? 2 : 0,
        child: CustomPaint(
          child: Container(
            height: shape.height,
          ),
          size: Size.fromHeight(shape.height),
          painter: indicatorPainter,
        ),
      ),
    );
  }
}

class OvalPainter extends CustomPainter {
  double page;
  int count;
  Color color;
  Color selectedColor;
  double padding;
  Paint _circlePaint;
  Paint _selectedPaint;
  Size size;

  OvalPainter({
    this.page = 0.0,
    this.count = 0,
    this.color = const Color(0xFFFFFFFF),
    this.selectedColor = Colors.grey,
    this.padding = 5.0,
    this.size,
  }) {
    _circlePaint = Paint();
    _circlePaint.color = color;

    _selectedPaint = Paint();
    _selectedPaint.color = selectedColor;

    this.page ??= 0.0;
    this.count ??= 0;
    this.color ??= Color(0xFFFFFFFF);
    this.selectedColor ??= Colors.grey;
    this.size ??= Size(12, 12);
    this.padding ??= 5.0;
  }
  double get totalWidth => count * size.width + padding * (count - 1);

  @override
  void paint(Canvas canvas, Size size) {
    var height = this.size.height;
    var width = this.size.width;
    var centerWidth = size.width / 2;
    var startX = centerWidth - totalWidth / 2;
    for (var i = 0; i < count ?? 0; i++) {
      var x = startX + i * (width + padding);
      var rect = Rect.fromLTWH(x, 0, width, height);
      canvas.drawOval(rect, _circlePaint);
    }

    var selectedX = startX + page * (width + padding);
    var rect = Rect.fromLTWH(selectedX, 0, width, height);
    canvas.drawOval(rect, _selectedPaint);
  }

  @override
  bool shouldRepaint(CustomPainter oldDelegate) => true;
}

class RRectPainter extends CustomPainter {
  double page;
  int count;
  Color color;
  Color selectedColor;
  double padding;
  Paint _circlePaint;
  Paint _selectedPaint;
  Size size;
  Size cornerSize;

  RRectPainter({
    this.page = 0.0,
    this.count = 0,
    this.color = const Color(0xFFFFFFFF),
    this.selectedColor = Colors.grey,
    this.padding = 5.0,
    this.size,
    this.cornerSize,
  }) {
    _circlePaint = Paint();
    _circlePaint.color = color;

    _selectedPaint = Paint();
    _selectedPaint.color = selectedColor;

    this.page ??= 0.0;
    this.count ??= 0;
    this.color ??= Color(0xFFFFFFFF);
    this.selectedColor ??= Colors.grey;
    this.size ??= Size(12, 12);
    this.padding ??= 5.0;
  }
  double get totalWidth => count * size.width + padding * (count - 1);

  @override
  void paint(Canvas canvas, Size size) {
    var height = this.size.height;
    var width = this.size.width;
    var centerWidth = size.width / 2;
    var startX = centerWidth - totalWidth / 2;
    for (var i = 0; i < count ?? 0; i++) {
      var x = startX + i * (width + padding);
      var rect = Rect.fromLTWH(x, 0, width, height);
      var rrect = RRect.fromRectAndRadius(
        rect,
        Radius.elliptical(cornerSize.width, cornerSize.height),
      );
      canvas.drawRRect(rrect, _circlePaint);
    }

    var selectedX = startX + page * (width + padding);
    var rect = Rect.fromLTWH(selectedX, 0, width, height);
    var rrect = RRect.fromRectAndRadius(
      rect,
      Radius.elliptical(cornerSize.width, cornerSize.height),
    );
    canvas.drawRRect(rrect, _selectedPaint);
  }

  @override
  bool shouldRepaint(CustomPainter oldDelegate) => true;
}

class CirclePainter extends CustomPainter {
  double page;
  int count;
  Color color;
  Color selectedColor;
  double radius;
  double padding;
  Paint _circlePaint;
  Paint _selectedPaint;

  CirclePainter({
    this.page = 0.0,
    this.count = 0,
    this.color = const Color(0xFFFFFFFF),
    this.selectedColor = Colors.grey,
    this.radius = 12.0,
    this.padding = 5.0,
  }) {
    _circlePaint = Paint();
    _circlePaint.color = color;

    _selectedPaint = Paint();
    _selectedPaint.color = selectedColor;

    this.page ??= 0.0;
    this.count ??= 0;
    this.color ??= Color(0xFFFFFFFF);
    this.selectedColor ??= Colors.grey;
    this.radius ??= 12.0;
    this.padding ??= 5.0;
  }

  double get totalWidth => count * radius * 2 + padding * (count - 1);

  @override
  void paint(Canvas canvas, Size size) {
    var centerWidth = size.width / 2;
    var startX = centerWidth - totalWidth / 2;
    for (var i = 0; i < count ?? 0; i++) {
      var x = startX + i * (radius * 2 + padding) + radius;
      canvas.drawCircle(Offset(x, radius), radius, _circlePaint);
    }

    var selectedX = startX + page * (radius * 2 + padding) + radius;
    canvas.drawCircle(Offset(selectedX, radius), radius, _selectedPaint);
  }

  @override
  bool shouldRepaint(CustomPainter oldDelegate) => true;
}
