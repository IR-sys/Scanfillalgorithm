# Scanfillalgorithm
triangle imoplementation using scan fill algorithm
#include<GL/glut.h>
//clear the current window and draw the triangle
void display(){
    //set every pixel in the frame buffer to the current clear color
    glClear(GL_COLOR_BUFFER_BIT);
    //Drawing is done by specifying sequence of vertices
    //the way vertices are connected depens on arguments to
    //glBegin.GL_POLYGON constructs filled polygon
    glBegin(GL_POLYGON);
    glcolor(1,0,0);glvertex(-0.6,-0.75,0.5);
    glcolor(0,1,0);glvertex(-0.6,-0.75,0);
    glcolor(0,0,1);glvertex(0,0.75,0);
    glEnd();
    //flush is drawing command buffer to make drawing happen as soon as possible
    glFlush();
}
//Initialize GLUT,display mode and main window;registers callbacks
//enters the main event loop
int main(int argc,char**argv){
    //uses a single buffer window in RGB mode
    //window or color index mode
    glutInit(&argc,argv);
    glutInitDisplayMode(GLUT_SINGLE||GLUT_RGB);
    //Position window at(80,80)-(480,380)and give its title
    glutInitWindowPosition(80,80);
    glutInitWindowSize(400,300);
    glutCreateWindow("A simple Triangle");
    glutDisplayFunc(display);
    glutMainLoop();

}
