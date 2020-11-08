package blockbattle

object main{
  def main(args: Array[String]): Unit = {
    val window = new BlockWindow((30,50),"BlockBattle")
    window.setBlock(Pos(15,15), java.awt.Color.BLUE)

    var quit = false
    while(!quit){
      var x = window.nextEvent(200)
      x match{
        case BlockWindow.Event.Undefined =>
        case BlockWindow.Event.WindowClosed => quit = true
        case _ => println(x)
      }
    }
  }
}
